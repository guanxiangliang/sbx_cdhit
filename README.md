# Sunbeam extension sbx_cdhit

This is a Sunbeam (https://github.com/sunbeam-labs) extension remove the sequncing reads after QC step. The process will remove similar reads using CD-HIT (https://jgi.doe.gov/data-and-tools/bbtools/bb-tools-user-guide/clumpify-guide/).  

# Installing and running

Activate sunbeam and clone the repo to `sunbeam/extension`
```
source activate sunbeam
cd $SUNBEAM_DIR
git clone https://github.com/guanzhidao/sbx_cdhit extensions/sbx_cdhit
conda install --file extensions/sbx_cdhit/requirements.txt
```

Remember to add cdhit option to your sunbeam config file
```
cat $SUNBEAM_DIR/extensions/sbx_cdhit/config.yml >> $PROJECT_DIR/sunbeam_config.yml
sunbeam run --configfile $PROJECT_DIR/sunbeam_config.yml all_cdhit
```

