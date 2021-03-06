# Upgrading Pre-Stack Pro

Updates for Pre-Stack Pro will be notified by email and will become available on [http://prestackpro.plan.io](http://prestackpro.plan.io) with your individual user account, if you have not obtained the credentials please contact [support@sharpreflections.com](https://github.com/sharpreflections/prestackpro-manual/tree/8bdcba1d7bdf85df36d1f4de36ef5e6a1172d09a/support@sharpreflections.com)

Installation and upgrades of Pre-Stack Pro must be done on ALL hosts, they require the same frontend and backend version to be able to run.  
TIP: If the parallel file system is already running, you might save time placing the Pre-Stack Pro binary on /data\_parallel/ for easier updating the remaining nodes.

To upgrade

```bash
rpm –U PreStackPRO-X.X.X.x86_64.rpm
```

Please verify that the filename and path is correct, if you download via Firefox the downloaded file will normally be stored in /home/USERNAME/Downloads/

If you get a warning about missing dependency “libibverbs” this could mean that you have some issues with the infiniband installation, please go back and verify that you followed all steps.

On frontend \(Client which is not supposed to be computing\) an infiniband connection is not required.

