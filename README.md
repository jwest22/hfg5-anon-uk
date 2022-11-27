# Hackathon for Good #5

### **Challenge:** Anonymisation of social media data
### **Team:** The Instagrammers

#### Repo Contents

**EMR Spark cluster-start-script.txt**
* Entire AWS CLI command to launch a new EMR on ECS Spark Cluster

**EMR Software-config.json**
* Spark configuration used during cluster provisioning. 
* JSL Documentation: https://nlp.johnsnowlabs.com/docs/en/install#emr-support

**Bootstrap.jar**
* Machine bootstrap script
* Installs:
  * aws cli
  * boto
  * spark-nlp
  * fsspec
  
 **HFGS-anon-yk.ipynb**
 * AWS EMR Studio Notebook
   * Imports all libraries & starts Spark session
   * Loads json file from S3
   * Creates pipeline using pretrained XLMRoBERTa model: https://huggingface.co/xlm-roberta-base
   * Fits json data to model
 
**Next Steps (TODO)**
* Resolve remaining bugs with model pipeline
* Test & evaluate model against multiple languages
* Cleanup/automate transfer process from S3->EMR->S3
* Develop infrastructure-as-code deployment
  * Terraform
  * Cloudformation
