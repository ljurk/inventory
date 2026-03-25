---
layout: default
title: Cable Inventory
---

## Available Cables

| Name | Length | Quantity | Link |
|------|--------|----------|------|
{% for cable in site.data.cables %}| {{ cable.name }} | {{ cable.length }}m  | {{ cable.quantity }} | [Link]({{ cable.link }}) |
{% endfor %}

## Fixtures

| Name | Quantity | Link | Manual |
|------|----------|------|--------|
{% for fixture in site.data.fixtures %}| {{ fixture.name }} | {{ fixture.quantity }} | [Link]({{ fixture.link }}) | {% if fixture.manual %}[Manual]({{ fixture.manual }}){% endif %} |
{% endfor %}

## Checkout

[Create Checkout Issue]({{ site.github_repo }}/issues/new?template=checkout.md)

## Past Checkouts

<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Event</th>
      <th>Issue</th>
    </tr>
  </thead>
  <tbody id="checkout-history">
    <tr><td colspan="3">Loading...</td></tr>
  </tbody>
</table>

[View all issues]({{ site.github_repo }}/issues?q=is%3Aissue+label%3Acheckout)
