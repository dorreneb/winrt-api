---
-api-id: T:Windows.Storage.StorageFile
-api-type: winrt class
---

<!-- Class syntax.
public class StorageFile : Windows.Storage.IStorageFile, Windows.Storage.IStorageFile2, Windows.Storage.IStorageFilePropertiesWithAvailability, Windows.Storage.IStorageItem, Windows.Storage.IStorageItem2, Windows.Storage.IStorageItemProperties, Windows.Storage.IStorageItemProperties2, Windows.Storage.IStorageItemPropertiesWithProvider, Windows.Storage.Streams.IInputStreamReference, Windows.Storage.Streams.IRandomAccessStreamReference
-->

# Windows.Storage.StorageFile

## -description

Represents a file. Provides information about the file and its content, and ways to manipulate them.

## -remarks

Typically, you access [StorageFile](storagefile.md) objects as the result of asynchronous method and/or function calls. For example, both of the static methods [GetFileFromPathAsync](storagefile_getfilefrompathasync_1252266672.md) and [GetFileFromApplicationUriAsync](storagefile_getfilefromapplicationuriasync_1702427701.md) return a [StorageFile](storagefile.md) that represents the specified file.

Additionally, whenever you call a file picker to let the user pick a file (or files) the file picker will return the file as a [StorageFile](storagefile.md).

> [!NOTE]
> [StorageFile](storagefile.md) objects can't represent files that are ".lnk", ".url", or ".wsh" file types.

## -examples

This example shows you how to call a file picker, using [FileOpenPicker.PickSingleFileAsync](../windows.storage.pickers/fileopenpicker_picksinglefileasync_1320627792.md) to capture and process a file that the users picks.

```csharp
var openPicker = new FileOpenPicker();
StorageFile file = await openPicker.PickSingleFileAsync();
// Process picked file
if (file != null)
{
    // Store file for future access
    Windows.Storage.AccessCache.StorageApplicationPermissions.FutureAccessList.Add(file);
}
else
{
    // The user didn't pick a file
}
```

```javascript

openPicker.pickSingleFileAsync().then(function (file) {
   if (file) {
       // Process picked file

       // Store file for future access
       var fileToken = Windows.Storage.AccessCache.StorageApplicationPermissions.futureAccessList.add(file);
   } else {
       // The user didn't pick a file
   }
});
```

After [PickSingleFileAsync](../windows.storage.pickers/fileopenpicker_picksinglefileasync_1320627792.md) completes, `file` gets the picked file as a [StorageFile](storagefile.md).

In the example, `openPicker` contains a [FileOpenPicker](../windows.storage.pickers/fileopenpicker.md) object. To learn more about using file picker see [Open files and folders with a picker](https://msdn.microsoft.com/library/f87dbe2f-77db-4573-8172-29e11abefd34).

Additionally, `fileToken` gets an identifier that you can use to retrieve the file from the [FutureAccessList](../windows.storage.accesscache/storageapplicationpermissions_futureaccesslist.md). To learn more about storing files and folders so you can access them again later, see [FutureAccessList](../windows.storage.accesscache/storageapplicationpermissions_futureaccesslist.md), [MostRecentlyUsedList](../windows.storage.accesscache/storageapplicationpermissions_mostrecentlyusedlist.md) and [How to track recently used files and folders](https://msdn.microsoft.com/library/7062d754-877e-4e59-a1ff-be0603020e6c).

## -see-also

[StorageFolder](storagefolder.md), [IStorageFile](istoragefile.md), [IStorageItem](istorageitem.md), [IRandomAccessStreamReference](../windows.storage.streams/irandomaccessstreamreference.md), [IInputStreamReference](../windows.storage.streams/iinputstreamreference.md), [IStorageItemProperties](istorageitemproperties.md), [IStorageItemProperties2](istorageitemproperties2.md), [IStorageItem2](istorageitem2.md), [IStorageItemPropertiesWithProvider](istorageitempropertieswithprovider.md), [IStorageFilePropertiesWithAvailability](istoragefilepropertieswithavailability.md), [Serializing and deserializing data sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DataReaderWriter), [File access sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/FileAccess)

## -capabilities

documentsLibrary, musicLibrary, picturesLibrary, videosLibrary
