## Aliyun OSS Adapter For Flysystem.

[![Author](http://img.shields.io/badge/author-@Joe-blue.svg?style=flat-square)](https://www.xxtime.com)
[![Code Climate](https://codeclimate.com/github/xxtime/flysystem-aliyun-oss/badges/gpa.svg)](https://codeclimate.com/github/xxtime/flysystem-aliyun-oss)
[![Travis CI](https://travis-ci.org/xxtime/flysystem-aliyun-oss.svg?branch=master)](https://travis-ci.org/xxtime/flysystem-aliyun-oss)
[![Total Downloads](https://img.shields.io/packagist/dt/xxtime/flysystem-aliyun-oss.svg?style=flat-square)](https://packagist.org/packages/xxtime/flysystem-aliyun-oss)

AliYun OSS Storage adapter for flysystem - a PHP filesystem abstraction.  

### Installation
composer require xxtime/flysystem-aliyun-oss

### Usage

```php
use League\Flysystem\Filesystem;
use Xxtime\Flysystem\Aliyun\OssAdapter;

$filesystem = new Filesystem(new OssAdapter([
    'access_id'     => 'access_key_id',
    'access_secret' => 'access_key_secret',
    'bucket'        => 'bucket name',

    // 'endpoint'       => 'oss-cn-shanghai.aliyuncs.com',
    // 'timeout'        => 3600,
    // 'connectTimeout' => 10,
]));


// Write Files
$filesystem->write('path/to/file.txt', 'contents');

// Update Files
$filesystem->update('path/to/file.txt', 'new contents');

// Check if a file exists
$exists = $filesystem->has('path/to/file.txt');

// Read Files
$contents = $filesystem->read('path/to/file.txt');

// Delete Files
$filesystem->delete('path/to/file.txt');

// Rename Files
$filesystem->rename('filename.txt', 'newname.txt');

// Copy Files
$filesystem->copy('filename.txt', 'duplicate.txt');
```

### Reference
[http://flysystem.thephpleague.com/api/](http://flysystem.thephpleague.com/api/)  
[https://github.com/thephpleague/flysystem](https://github.com/thephpleague/flysystem)  
[https://help.aliyun.com/document_detail/32099.html](https://help.aliyun.com/document_detail/32099.html)  

