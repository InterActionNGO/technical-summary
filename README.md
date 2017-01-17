# NGO Aid Map
##### A Technical Summary

### Overview of the Application
NGO Aid Map is a dynamic, interactive web application designed to showcase the work of non-profit organizations' work in international development and humanitarian assistance through a user-friendly map interface.

Participating organizations may own one or more user accounts through which they can manage their project and organization data from a simple, easy-to-use admin portal. Active projects are visualized automatically on the public site, where anyone can view, filter, download, and analyze the information to their heart's content. An in-depth [reporting feature](https://ngoaidmap.org/p/analysis) also provides robust query and analysis capabilities.

##### Brief History
NGO Aid Map is an [InterAction](https://www.interaction.org) initiative, first conceptualized in 2009 as food security mapping exercise. It debuted in 2011, quite unexpectedly, as Haiti Aid Map after the earthquake to show who was doing what, where, in the relief effort. Since then, it has grown significantly in features and in quanitity and quality of information available, now containing data for all sectors within aid and development globally.

##### Contributors
The initiative has been made possible through funding by the [International Fund for Agricultural Development](https://www.ifad.org/) (IFAD) and [FedEx](http://www.fedex.com/) and technical contributions of [vizzuality.](http://www.vizzuality.com/), [Simbiotica](http://simbiotica.es/) (now vizzuality.), and [Viget](https://www.viget.com/).

### About the Data
##### Open
All of the data on [NGO Aid Map](https://ngoaidmap.org) is voluntarily provided by [InterAction](https://www.interaction.org) members and is made freely available to the public under the [Open Data Commons Attribution License v1.0](http://opendatacommons.org/licenses/by/1.0/) (ODC-By v1.0).

##### Accessible
Datasets are available for **download in CSV format** on each level of navigation on the site. Active projects are exported by default, but a full dataset including closed projects may be downloaded by removing the `&status=active` text from the end of the download link url.

A beta-version **RESTful API** is also available for developers and contains JSON-formatted project information (also available in CSV format) as well as info on organizations, sectors, and geolocations.  Read the [documentation](https://ngoaidmap.org/docs) for more information.  Please note that the API is in early development and is subject to change at any time without notice. If you have any questions, please email us at mappinginfo@interaction.org.

##### Interoperable
Project data is also available in **IATI\* XML** format for publication to the [IATI Registry](https://iatiregistry.org), a repository of international aid data in a standardized, machine-readable format.  Excepting organizations that publish independently, organization datasets on NGO Aid Map are published to the registry daily.

Read more on the NGO Aid Map [data page](https://ngoaidmap.org/p/data) and feel free to [email us](mailto:mappinginfo@interaction.org).

*_International Aid Transparency Initiative_ ([Read More](https://iatistandard.org))

### Use it. Improve it. Cite it.
NGO Aid Map is an open-source project, released under the [GNU Affero General Public License v3 (GNU AGPLv3)](https://www.gnu.org/licenses/agpl-3.0.html) on GitHub in a [front end](https://github.com/InterActionNGO/ngoaidmap) and a [back end](https://github.com/InterActionNGO/NGO-admin) repository.  Contributions are welcome!

### Needs
##### API
In the **short term**, the API would benefit from better implementation of existing features.  This would entail auditing all the existing endpoints to verify response integrity and timeliness and ensure the content and structure aligns with current specifications.  Some endpoints may need to be added, others revised or retired.  The existing documentation needs to be updated to reflect the revisions and be revised for accuracy and readability.

**Long term**, we must address user management and infrastucture needs so the API can be a scaleable, reliable resource for many, tiered-authentication users.  This includes:
- Addition of API user accounts and API keys to manage and track usage
- Addition of **CREATE**, **UPDATE**, and **DELETE** methods to allow for complete data management via the API
- Deployment of the API where it will have ample resources to meet growing demand (For example, will this mean hosting the API on a dedicated server, or perhaps using an auto-scaling cloud service)
- Thorough, clear documentation

### Technical Implementation
Many open-source applications work together to power NGO Aid Map and make it feature-rich, cross-browser, and platform-indepedent. Most notably, it is built using the [Rails](http://rubyonrails.org/) framework for the [Ruby](https://www.ruby-lang.org/) programming language. Following is a list of several other major components that drive the platform:
- [PostgreSQL](https://www.postgresql.org/)
- [CARTO](https://carto.com)
- [PostGIS](http://postgis.net/)
- [LeafletJs](http://leafletjs.com/)
- [NodeJs](http://nodejs.org/)
- [Redis](https://redis.io/)

For a complete list, including javascript libraries, templating engines, style extensions, and more, checkout the [source code](https://github.com/InterActionNGO/ngoaidmap) on GitHub. Want to get your own instance of NGO Aid Map up and running? Just follow the instructions in the [README.md](https://github.com/InterActionNGO/ngoaidmap/blob/master/README.md).
