#Swift Object Store

##Object Store
```
Object Storage (also known as object-based storage) is a storage architecture that manages data as objects,
as opposed to other storage architectures like file systems which manage data as a file hierarchy and
block storage which manages data as blocks within sectors and tracks.
```

####Access via API at application-level, rather than via OS at filesystem-level
```
1) byte-level interaction is not possible. Instead, entire objects are stored or retrieved with a single command.

2)Interaction can occur via a single API endpoint

3)Object Storage is one (or potentially few in the case of multi-region deployments) giant volume.
```
####No directory tree (uses containers vs. a directory tree)
```
 allows for massive scalability: by eliminating the overhead of keeping track of large quantities of directory metadata
```
#### Metadata lives with the object
```
 In an Object Storage system, there is no scalability issue, as this data lives directly with the object, 
and can be retrieved with a single API call without the overhead associated with a relational database.
```
#### Backups/Archives
```
Object Storage systems have internal mechanisms to verify file consistency,
and handle failed drives, bit-rot, server and cabinet failures, etc.
```
#### Erasure coding (EC)
```
It is a method of data protection in which data is broken into fragments,
expanded and encoded with redundant data pieces and 
stored across a set of different locations or storage media.
```
####RAID 
```
(originally redundant array of inexpensive disks, now commonly redundant array of independent disks)
is a data storage virtualization technology that combines multiple physical disk drive components 
into a single logical unit for the purposes of data redundancy, performance improvement, or both.
```
### Contents


* [Articles](#articles)
* [Guides](#guides)
* [Language-specific](#language-specific)
    * [Python](#python)
* [Videos](#videos)
* [other repos](#similar-github-repos)


## Articles

* Recommended:  Jonathan Kelly – **Introduction To Object Storage** [[web][a_sy]]
* Jonathan Kelly - **What Can Object Storage Do For Me Today?** [[web][a_ss]]
* 
[a_sy]: http://www.rackspace.com/blog/introduction-to-object-storage/
[a_ss]: http://www.rackspace.com/blog/what-can-object-storage-do-for-me-today/
