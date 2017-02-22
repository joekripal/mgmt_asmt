## External Entities
* **Developer** - Person looking for vulnerabilities and licenses in a software.
* **Manager** - Person in charge of gathering and modifying policies.

## Data Repositories
* **License & Vulnerability Database** - Data repository that license and vulnerability results are sent to be retrieved by developers or managers.
* **NIST Vulnerability DB** - National Institute of Standards and Technology open source data repository for known vulnerabilities of software.
* **Policy DB** - Data Repository for policies set by managers.

## Processes
* **License Scanner** - Software that scans other software for licenses and sends back results to requester.
* **Retrieve Policies** - Sends policy request to Policy DB and sends policy results to Manager.
* **Retrieve Licenses & Vulnerabilities** - Takes request from Manager or Developer and sends it to License & Vulnerability Database. Also sends License & Vulnerability Results back to Manager or Developer.
* **Scan Software for Vulnerabilities & Licenses** - Takes software from Developer and sends it to the License Scanner. Sends Software Name to NIST Vulnerability DB. Recieves License Results from License Scanner and Vulnerability Results from NIST Vulnerability DB. Sends License Results and Vulnerability Results back to Developer as well as to License & Vulnerability Database.
* **Set Policies** - Sends a new policy or a policy change from the Manager to the Policy DB.

## Data Flows
* **License & Vulnerability Request** - Sent by either Developer or Manager to find Licenses and Vulnerabilities for a given piece of software.
* **License & Vulnerability Results** - Information on the licenses and vulnerabilities of a given piece of software.
* **License Results** - Results on any relevant licenses from the License Scanner sent back to the Developer and stored in the License & Vulnerability Database.
* **Policy Change** - Manager sends this to Policy DB in order to change a current policy, add a new policy, or remove an old policy.
* **Policy Request** - Manager sends this request to Policy DB to retrieve the necessary policies.
* **Policy Results** - Detailed results sent from Policy DB to Manager on policies that were requested.
* **Software** - The actual software the Developer is looking to utilize.
* **Software Name** - Only the name of the software so the NIST Vulnerability DB can look to see if there are any known vulnerabilities in software under the same name.
* **Vulnerability Results** - Results from the NIST Vulnerability DB sent back to the Developer and also stored in the License & Vulnerability Database.
