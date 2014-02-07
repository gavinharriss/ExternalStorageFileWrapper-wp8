ExternalStorageFileWrapper-wp8
==============================

ExternalStorageFile stream bug fix for Windows Phone 8

A wrapper that can be used to circumnavigate the Seek() bug present in the stream object returned by ExternalStorageFile.OpenForReadAsync() on Windows Phone 8.

Code example:

ExternalStorageFile file = await device.GetFileAsync(filename); // device is an instance of ExternalStorageDevice
Stream streamOriginal = await file.OpenForReadAsync();
ExternalStorageFileWrapper streamToUse = new ExternalStorageFileWrapper(streamOriginal);
