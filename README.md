# api documentation for  [decompress-zip (v0.3.0)](https://github.com/bower/decompress-zip#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-decompress-zip.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-decompress-zip) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-decompress-zip.svg)](https://travis-ci.org/npmdoc/node-npmdoc-decompress-zip)
#### Extract files from a ZIP archive

[![NPM](https://nodei.co/npm/decompress-zip.png?downloads=true)](https://www.npmjs.com/package/decompress-zip)

[![apidoc](https://npmdoc.github.io/node-npmdoc-decompress-zip/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-decompress-zip_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-decompress-zip/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-decompress-zip/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-decompress-zip/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Bower"
    },
    "bin": {
        "decompress-zip": "bin/decompress-zip"
    },
    "bugs": {
        "url": "https://github.com/bower/decompress-zip/issues"
    },
    "dependencies": {
        "binary": "^0.3.0",
        "graceful-fs": "^4.1.3",
        "mkpath": "^0.1.0",
        "nopt": "^3.0.1",
        "q": "^1.1.2",
        "readable-stream": "^1.1.8",
        "touch": "0.0.3"
    },
    "description": "Extract files from a ZIP archive",
    "devDependencies": {
        "archiver": "^0.13.1",
        "chai": "^1.10.0",
        "coveralls": "^2.11.2",
        "fs-jetpack": "^0.5.3",
        "grunt": "^0.4.1",
        "grunt-cli": "^0.1.13",
        "grunt-contrib-jshint": "^0.11.0",
        "grunt-contrib-watch": "^0.6.1",
        "grunt-exec": "^0.4.2",
        "grunt-simple-mocha": "^0.4.0",
        "istanbul": "^0.3.5",
        "mocha": "^2.1.0",
        "tmp": "0.0.24"
    },
    "directories": {},
    "dist": {
        "shasum": "ae3bcb7e34c65879adfe77e19c30f86602b4bdb0",
        "tarball": "https://registry.npmjs.org/decompress-zip/-/decompress-zip-0.3.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "files": [
        "bin",
        "lib"
    ],
    "gitHead": "e0f4c0b3e3aede745929cfbcdd85c19613116ab0",
    "homepage": "https://github.com/bower/decompress-zip#readme",
    "keywords": [
        "zip",
        "unzip",
        "tar",
        "untar",
        "compress",
        "decompress",
        "archive",
        "extract",
        "zlib"
    ],
    "license": "MIT",
    "main": "lib/decompress-zip.js",
    "maintainers": [
        {
            "name": "wibblymat",
            "email": "mat@wibbly.org.uk"
        },
        {
            "name": "paulirish",
            "email": "paul.irish@gmail.com"
        },
        {
            "name": "sheerun",
            "email": "sheerun@sher.pl"
        },
        {
            "name": "sindresorhus",
            "email": "sindresorhus@gmail.com"
        },
        {
            "name": "satazor",
            "email": "andremiguelcruz@msn.com"
        },
        {
            "name": "desandro",
            "email": "desandrocodes@gmail.com"
        }
    ],
    "name": "decompress-zip",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/bower/decompress-zip.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module decompress-zip](#apidoc.module.decompress-zip)
1.  [function <span class="apidocSignatureSpan">decompress-zip.</span>super_ ()](#apidoc.element.decompress-zip.super_)
1.  object <span class="apidocSignatureSpan">decompress-zip.</span>extractors
1.  object <span class="apidocSignatureSpan">decompress-zip.</span>structures

#### [module decompress-zip.extractors](#apidoc.module.decompress-zip.extractors)
1.  [function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>copy (file, destination, zip, basePath)](#apidoc.element.decompress-zip.extractors.copy)
1.  [function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>deflate (file, destination, zip)](#apidoc.element.decompress-zip.extractors.deflate)
1.  [function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>folder (folder, destination, zip)](#apidoc.element.decompress-zip.extractors.folder)
1.  [function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>store (file, destination, zip)](#apidoc.element.decompress-zip.extractors.store)
1.  [function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>symlink (file, destination, zip, basePath)](#apidoc.element.decompress-zip.extractors.symlink)

#### [module decompress-zip.structures](#apidoc.module.decompress-zip.structures)
1.  [function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readDirectory (buffer)](#apidoc.element.decompress-zip.structures.readDirectory)
1.  [function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readEndRecord (buffer)](#apidoc.element.decompress-zip.structures.readEndRecord)
1.  [function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readFileEntry (buffer)](#apidoc.element.decompress-zip.structures.readFileEntry)
1.  number <span class="apidocSignatureSpan">decompress-zip.structures.</span>maxFileEntrySize



# <a name="apidoc.module.decompress-zip"></a>[module decompress-zip](#apidoc.module.decompress-zip)

#### <a name="apidoc.element.decompress-zip.super_"></a>[function <span class="apidocSignatureSpan">decompress-zip.</span>super_ ()](#apidoc.element.decompress-zip.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.decompress-zip.extractors"></a>[module decompress-zip.extractors](#apidoc.module.decompress-zip.extractors)

#### <a name="apidoc.element.decompress-zip.extractors.copy"></a>[function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>copy (file, destination, zip, basePath)](#apidoc.element.decompress-zip.extractors.copy)
- description and source-code
```javascript
copy = function (file, destination, zip, basePath) {
    var type;
    var parent = path.dirname(destination);

    return mkdir(parent, zip.dirCache)
    .then(function () {
        return getLinkLocation(file, destination, zip, basePath);
    })
    .then(function (linkTo) {
        return stat(path.resolve(parent, linkTo))
        .then(function (stats) {
            if (stats.isFile()) {
                type = 'File';
                var input = new stream.Readable();
                input.wrap(fs.createReadStream(path.resolve(parent, linkTo)));
                return pipePromise(input, destination);
            } else if (stats.isDirectory()) {
                type = 'Directory';
                return mkdir(destination, zip.dirCache);
            } else {
                throw new Error('Could not follow symlink to unknown file type');
            }
        })
        .then(function () {
            return {copy: file.path, original: linkTo, type: type};
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.extractors.deflate"></a>[function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>deflate (file, destination, zip)](#apidoc.element.decompress-zip.extractors.deflate)
- description and source-code
```javascript
deflate = function (file, destination, zip) {
    // For Deflate you don't actually need to specify the end offset - and
    // in fact many ZIP files don't include compressed file sizes for
    // Deflated files so we don't even know what the end offset is.

    return mkdir(path.dirname(destination), zip.dirCache)
    .then(function () {
        if (file._maxSize <= zip.chunkSize) {
            return zip.getBuffer(file._offset, file._offset + file._maxSize)
            .then(inflateRaw)
            .then(function (buffer) {
                return writeFile(destination, buffer, { mode: file.mode });
            });
        } else {
            // For node 0.8 we need to create the Zlib stream and attach
            // handlers in the same tick of the event loop, which is why we do
            // the creation in here
            var input = new stream.Readable();
            input.wrap(fs.createReadStream(zip.filename, {start: file._offset}));
            var inflater = input.pipe(zlib.createInflateRaw({highWaterMark: 32 * 1024}));

            return pipePromise(inflater, destination, { mode: file.mode });
        }
    })
    .then(function () {
        return {deflated: file.path};
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.extractors.folder"></a>[function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>folder (folder, destination, zip)](#apidoc.element.decompress-zip.extractors.folder)
- description and source-code
```javascript
folder = function (folder, destination, zip) {
    return mkdir(destination, zip.dirCache, folder.mode)
    .then(function () {
        return {folder: folder.path};
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.extractors.store"></a>[function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>store (file, destination, zip)](#apidoc.element.decompress-zip.extractors.store)
- description and source-code
```javascript
store = function (file, destination, zip) {
    var writer;

    if (file.uncompressedSize === 0) {
        writer = touch.bind(null, destination);
    } else if (file.uncompressedSize <= zip.chunkSize) {
        writer = function () {
            return zip.getBuffer(file._offset, file._offset + file.uncompressedSize)
            .then(function (buffer) {
                return writeFile(destination, buffer, { mode: file.mode });
            });
        };
    } else {
        var input = new stream.Readable();
        input.wrap(fs.createReadStream(zip.filename, {start: file._offset, end: file._offset + file.uncompressedSize - 1}));
        writer = pipePromise.bind(null, input, destination, { mode: file.mode });
    }

    return mkdir(path.dirname(destination), zip.dirCache)
    .then(writer)
    .then(function () {
        return {stored: file.path};
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.extractors.symlink"></a>[function <span class="apidocSignatureSpan">decompress-zip.extractors.</span>symlink (file, destination, zip, basePath)](#apidoc.element.decompress-zip.extractors.symlink)
- description and source-code
```javascript
symlink = function (file, destination, zip, basePath) {
    var parent = path.dirname(destination);
    return mkdir(parent, zip.dirCache)
    .then(function () {
        return getLinkLocation(file, destination, zip, basePath);
    })
    .then(function (linkTo) {
        return symlink(path.resolve(parent, linkTo), destination)
        .then(function () {
            return {symlink: file.path, linkTo: linkTo};
        });
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.decompress-zip.structures"></a>[module decompress-zip.structures](#apidoc.module.decompress-zip.structures)

#### <a name="apidoc.element.decompress-zip.structures.readDirectory"></a>[function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readDirectory (buffer)](#apidoc.element.decompress-zip.structures.readDirectory)
- description and source-code
```javascript
readDirectory = function (buffer) {
    var directory = [];
    var current;
    var index = 0;

    while (index < buffer.length) {
        current = binary.parse(buffer.slice(index, index + 46))
        .word32lu('signature')
        .word8lu('creatorSpecVersion')
        .word8lu('creatorPlatform')
        .word8lu('requiredSpecVersion')
        .word8lu('requiredPlatform')
        .word16lu('generalPurposeBitFlag')
        .word16lu('compressionMethod')
        .word16lu('lastModFileTime')
        .word16lu('lastModFileDate')
        .word32lu('crc32')
        .word32lu('compressedSize')
        .word32lu('uncompressedSize')
        .word16lu('fileNameLength')
        .word16lu('extraFieldLength')
        .word16lu('fileCommentLength')
        .word16lu('diskNumberStart')
        .word16lu('internalFileAttributes')
        .word32lu('externalFileAttributes')
        .word32lu('relativeOffsetOfLocalHeader')
        .vars;

        index += 46;

        current.generalPurposeFlags = convertGeneralPurposeFlags(current.generalPurposeBitFlag);
        current.fileAttributes = parseExternalFileAttributes(current.externalFileAttributes, current.creatorPlatform);

        current.modifiedTime = convertDateTime(current.lastModFileDate, current.lastModFileTime);
        current.fileName = current.extraField = current.fileComment = '';
        current.headerLength = 46 + current.fileNameLength + current.extraFieldLength + current.fileCommentLength;

        if (current.fileNameLength > 0) {
            current.fileName = buffer.slice(index, index + current.fileNameLength).toString();
            index += current.fileNameLength;
        }

        if (current.extraFieldLength > 0) {
            current.extraField = buffer.slice(index, index + current.extraFieldLength).toString();
            index += current.extraFieldLength;
        }

        if (current.fileCommentLength > 0) {
            current.fileComment = buffer.slice(index, index + current.fileCommentLength).toString();
            index += current.fileCommentLength;
        }

        if (current.fileAttributes.type !== 'Directory' && current.fileName.substr(-1) === '/') {
            // TODO: check that this is a reasonable check
            current.fileAttributes.type = 'Directory';
        }

        directory.push(current);
    }

    directory.sort(directorySort);

    return directory;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.structures.readEndRecord"></a>[function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readEndRecord (buffer)](#apidoc.element.decompress-zip.structures.readEndRecord)
- description and source-code
```javascript
readEndRecord = function (buffer) {
    var data = binary.parse(buffer)
    .word32lu('signature')
    .word16lu('diskNumber')
    .word16lu('directoryStartDisk')
    .word16lu('directoryEntryCountDisk')
    .word16lu('directoryEntryCount')
    .word32lu('directorySize')
    .word32lu('directoryOffset')
    .word16lu('commentLength')
    .buffer('comment', 'commentLength')
    .vars;

    data.comment = data.comment.toString();

    return data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.decompress-zip.structures.readFileEntry"></a>[function <span class="apidocSignatureSpan">decompress-zip.structures.</span>readFileEntry (buffer)](#apidoc.element.decompress-zip.structures.readFileEntry)
- description and source-code
```javascript
readFileEntry = function (buffer) {
    var index = 0;

    var fileEntry = binary.parse(buffer.slice(index, 30))
    .word32lu('signature')
    .word16lu('versionNeededToExtract')
    .word16lu('generalPurposeBitFlag')
    .word16lu('compressionMethod')
    .word16lu('lastModFileTime')
    .word16lu('lastModFileDate')
    .word32lu('crc32')
    .word32lu('compressedSize')
    .word32lu('uncompressedSize')
    .word16lu('fileNameLength')
    .word16lu('extraFieldLength')
    .vars;

    index += 30;

    fileEntry.fileName = fileEntry.extraField = '';

    fileEntry.entryLength = 30 + fileEntry.fileNameLength + fileEntry.extraFieldLength;

    if (fileEntry.entryLength > structures.maxFileEntrySize) {
        throw new Error('File entry unexpectedly large: ' + fileEntry.entryLength + ' (max: ' + structures.maxFileEntrySize + ')');
    }

    if (fileEntry.fileNameLength > 0) {
        fileEntry.fileName = buffer.slice(index, index + fileEntry.fileNameLength).toString();
        index += fileEntry.fileNameLength;
    }

    if (fileEntry.extraFieldLength > 0) {
        fileEntry.extraField = buffer.slice(index, index + fileEntry.extraFieldLength).toString();
        index += fileEntry.extraFieldLength;
    }

    return fileEntry;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
