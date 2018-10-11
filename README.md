# EnphaseInterface
Python implementation interface to the Enphase Developer API

## Installation

`python3 -m pip install pyenface`

## Usage

```python
from pyEnFace.EnphaseInterface import PandasEnphaseInterface

client = client = PandasEnphaseInterface(userId=<YOUR USERID>, api_key=<YOUR API KEY>)

# Request all systems
client.index()

# Request inventory
client.inventory(system_id=<SYSTEM ID>)

# Summary
client.summary(system_id=<SYSTEM ID>)

# Get data as pandas dataframe
start = pd.Timestamp('20180101')

client.energy_lifetime(system_id=<SYSTEM ID>, start_date=start)
```