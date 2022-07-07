# Mirth Resources REST API
A REST API for providing programmatic access to Mirth resources.

## Releases Listing
> POST https://mirth.brightcodecompany.com/resource/releases

Releases endpoint provides download links for different releases of Mirth Connect. You can search for a specific release by specifying parameters in your request body. </br>
**All data is parsed from the [official Connect repository](https://github.com/nextgenhealthcare/connect/releases/) and belongs to NextGen!**

**Be a good samaritan and don't abuse mine or NextGen's resources.**

Available values for request parameters:
| Parameter  | Available values |
| ------------- | ------------- |
| version | Pretty much all Mirth versions starting from 3.6.0 |
| os | windows, linux, mac os x  |
| arch | x86, x64  |
| download_type | installer, tar.gz, zip, rpm  |

### Request example
```json
{
    "version": "3.10.0",
    "os": "windows",
    "arch": "x64",
    "download_type": "installer"
} 
```
### Response example
```json
{
    "version": "3.10.0",
    "os": "windows",
    "arch": "x64",
    "download_type": "installer",
    "download_url": "https://s3.amazonaws.com/downloads.mirthcorp.com/connect/3.10.0.b2566/mirthconnect-3.10.0.b2566-windows-x64.exe",
    "sha256": "290fc631bb42d777796522425f070c86f71673db1c9571bbb344ff6090702cc5",
    "md5": "94019ee8496da751ec88da1dfbd917fd",
    "published_at": "2020-11-13 00:01:00.0"
}
```
