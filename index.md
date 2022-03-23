## Model Overview

The model we discuss here was created in an iterative process during initial passes of the surveyed literature: A superset of reported attributes was created, similar concepts (or identical concepts with different names) were grouped together and categories were defined in accordance to the typical section structure of the papers. This process resulted in the following *categories*:
[Technical aspects of recording](#technical-aspects-of-recording),
[Task description](#task-description),
[Participants](#participants),
[Experiment flow](#experiment-flow),
[Data processing](#data-processing), and
[Brain signal integration](#brain-signal-integration).

In the tables below, we present the experiment model for HCI research with brain signals. We describe each category and list the attributes contained within them. For each attribute, we give a definition of the attribute and present an example taken from the surveyed literature. We tried to identify examples which are biased towards a more detailed documentation, but individual examples may still lack certain information.

We invite the community to [contribute](#contribute) to future versions of the experiment model.

### Technical Aspects of Recording

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_technical %}
    {% if forloop.first %}
    <tr class="header">
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">"{{row['Example']}}" {% cite {{row['example_ref']}} %}</td>
    </tr>
  {% endfor %}
</table>

### Task Description

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_task %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">{% if row['Example'] %}"{{row['Example']}}" {% cite {{row['example_ref']}} %} {% endif %}</td>
    </tr>
  {% endfor %}
</table>


### Participants

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_participants %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">"{{row['Example']}}" {% cite {{row['example_ref']}} %}</td>
    </tr>
  {% endfor %}
</table>

### Experiment Flow

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_experiment %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">"{{row['Example']}}" {% cite {{row['example_ref']}} %}</td>
    </tr>
  {% endfor %}
</table>

### Data Processing

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_data %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">"{{row['Example']}}" {% cite {{row['example_ref']}} %}</td>
    </tr>
  {% endfor %}
</table>

### Brain Signal Integration

<table>
    <colgroup>
        <col width="30%" />
        <col width="40%" />
        <col width="30%" />
    </colgroup>
  {% for row in site.data.model_brain_signals %}
    {% if forloop.first %}
    <tr>
      {% for pair in row limit:3 %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
    <tr class="row">
        <td markdown="span">{{row['Attribute']}}</td>
        <td markdown="span">{{row['Description']}}</td>
        <td markdown="span">"{{row['Example']}}" {% cite {{row['example_ref']}} %}</td>
    </tr>
  {% endfor %}
</table>

### References

{% bibliography  --cited%}

## Contribute
To contribute to the {{ page.title }}, please consider submitting a pull request to our [Experiment Model for Brain Signals in HCI GitHub](https://github.com/brain-signals-hci/experiment-model/). You can suggest changes to existing attributes, descriptions, or examples. Or you can add new attributes to expand the experiment model. If you do so, please provide a name, description, and example from the literature (including references). For editing, provide your changes to the [Experiment Model File](https://github.com/brain-signals-hci/experiment-model/blob/main/brainsignal_hci_model.xlsx), add references to the [bibtex file](https://github.com/brain-signals-hci/experiment-model/blob/main/_bibliography/references.bib), and open a pull request with your changes.
Every pull request will be open for discussions.
