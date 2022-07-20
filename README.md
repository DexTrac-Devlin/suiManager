# suiManager
Single script to deploy and upgrade your Mysten Sui node

#### This has been tested on Debian 10 & 11.

(use at your own risk, consider this as 100% untested)

---
## General Directions
* Clone this repository
* Change directories into the new directory (```cd suiManager```)
* Add executable permissions to the ```chmod +x suiManager``` file
* Run the script (```suiManager -h```)

---
## Utilization

--
### Deploy New Mysten Sui Node
* This will:
  * Clone the Mysten Sui repository.
  * Create the necessary directories.
  * Download the genesis.blob file.
  * Deploy a new Mysten Sui node as a service (suid.service).
  
```bash
sudo ./suiManager -d
```


--
### Upgrade Existing Mysten Sui Node
* This will:
  * Stop the current suid.service.
  * Remove all outdated files.
  * Clone the repository.
  * Download the new genesis.blob.
  * Start the suid.service.

```bash
sudo ./suiManager -u
```



--
### Print Supported Options
* This will:
  * Print all supported command options

```bash
./suiManager -h
```
