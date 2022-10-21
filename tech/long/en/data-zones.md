# Data Zones

Data Zones is the physical or logical segmentation of data in a data lake to keep the data more secure or organized.

Data Zones are also referred to as Data Lake Zones, a data lake being a large repository for file or blob storage, usually files without a specific structure.

Data Zones are closely associated with cloud services and big data.

## Zones

The name for zones can vary across implementations. However, the Raw Zone is common across specifications. Trusted and Refined are other common names for zones.

### Transient

Transient zones is where the data first ingresses into the system, it is unprocessed or assessed so sensitive data is unencrpted. The transient zone is simply an intermediary landing zone before being identified and moved to its initial resting place in the raw zone.

### Raw

Raw zones is where data first comes to rest in the data lake, though it still may be promoted to other zones.

Raw zones are a common zone among all data zone specifications. Raw data is the zone in which the data is kept after ingressing the network. As it comes to rest in the network, sensitve data will need to be processed and encrypted but otherwise the data still exists in its original state.

Otherwise, the data in the raw zone is not bound by any rules or expectations. The data is not yet processed for any business or regulatory requirements.

### Trusted

Trusted zones is data that has been processed and accepted as the authoritative data source, or single source of truth for data through out the organizations system.

Data in trusted zones is largely immutable. The data has been processed as much as it is expected to be processed and has reached a static point where no further information will be aggregated into the data and all components of an organization agree to its completeness as a single source of truth.

Trusted data is considered a source of truth for the **ENTIRE** system.

### Refined

Refined data is data that has been manipulated or otherwise interpretted from the raw data in order to make it more useful. Refined data might be aggregated data, data with more meaning added, or data with some non-useful parts removed. Sometimes this is referred to as enrichment.

Microsoft calles this zone Curated.

Refined data applies to certain organizational units or sections of the organization. The value added or derived usually only applies to the specific business unit that it is intended for and is therefor specific for that system segment.

Refined data is a source truth ONLY for the the intended business unit it is refined for.

When refined data becomes complete and accurate such that the entire system/organization agrees to its correctness/completeness it will be promoted to trusted data.

## Key Ideas

Data Zones segment data into logical groups.

Data may be promoted in zones as the system/organization agrees to its completeness and correctness.

Data Zones bind data to business rules.

Data marts are groups of data bound to common business rules.

Sensitive data needs to be encrypted by the time it hits the raw zone.

## References

[1] https://www.healthcatalyst.com/insights/four-essential-zones-healthcare-data-lake
[2] https://dzone.com/articles/data-lake-governance-best-practices
[3] https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/best-practices/data-lake-zones
[4] https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/best-practices/data-lake-zones