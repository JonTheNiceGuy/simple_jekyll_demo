Hello, and welcome to this Jekyll Site!

<h1>Desktop GUI Clients</h1>
{% assign clients = site.data.Desktop | sort %}
{% for client_hash in clients %}
{% assign client = client_hash[1] %}
{% assign client_name = client_hash[0] | replace: '_', ' ' %}

* Client: {% if client.name %}{{ client.name }}{% else %}{{ client_name }}{% endif %}
{% if client.version %}  * {{ client.version }}{% endif %}
{% if client.description %}  * {{ client.description }}{% endif %}
  * Downloads{% if client.download.linux %}
    * [Linux]({{ client.download.linux }}){% endif %}{% if client.download.mac %}
    * [OSx]({{ client.download.mac }}){% endif %}{% if client.download.windows %}
    * [Windows]({{ client.download.windows }}){% endif %}
{% endfor %}

<h1>Desktop CLI Clients</h1>
{% assign clients = site.data.CLI | sort %}
{% for client_hash in clients %}
{% assign client = client_hash[1] %}
{% assign client_name = client_hash[0] | replace: '_', ' ' %}

* Client: {% if client.name %}{{ client.name }}{% else %}{{ client_name }}{% endif %}
{% if client.version %}  * {{ client.version }}{% endif %}
{% if client.description %}  * {{ client.description }}{% endif %}
  * Downloads{% if client.download.linux %}
    * [Linux]({{ client.download.linux }}){% endif %}{% if client.download.mac %}
    * [OSx]({{ client.download.mac }}){% endif %}{% if client.download.windows %}
    * [Windows]({{ client.download.windows }}){% endif %}{% if client.download.itunes %}
    * [iTunes Store]({{ client.download.itunes }}){% endif %}{% if client.download.googleplay %}
    * [Google Play Store]({{ client.download.googleplay }}){% endif %}{% if client.download.amazonapp %}
    * [Amazon App Store]({{ client.download.amazonapp }}){% endif %}{% if client.download.fdroid %}
    * [F-Droid]({{ client.download.fdroid }}){% endif %}{% if client.download.dat %}
    * [Dat]({{ client.download.dat }}){% endif %}
{% endfor %}

<h1>Mobile Apps</h1>
{% assign clients = site.data.Mobile | sort %}
{% for client_hash in clients %}
{% assign client = client_hash[1] %}
{% assign client_name = client_hash[0] | replace: '_', ' ' %}

* Client: {% if client.name %}{{ client.name }}{% else %}{{ client_name }}{% endif %}
{% if client.version %}  * {{ client.version }}{% endif %}
{% if client.description %}  * {{ client.description }}{% endif %}
  * Downloads{% if client.download.itunes %}
    * [iTunes Store]({{ client.download.itunes }}){% endif %}{% if client.download.googleplay %}
    * [Google Play Store]({{ client.download.googleplay }}){% endif %}{% if client.download.amazonapp %}
    * [Amazon App Store]({{ client.download.amazonapp }}){% endif %}{% if client.download.fdroid %}
    * [F-Droid]({{ client.download.fdroid }}){% endif %}{% if client.download.dat %}
    * [Dat]({{ client.download.dat }}){% endif %}
{% endfor %}
