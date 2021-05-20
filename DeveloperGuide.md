---
layout: page
title: DeveloperGuide
permalink: /developer-guide/
---

* Table of Contents
{:toc}

---

<div style="page-break-after: always;"></div>

# BC-TECH - Developer Guide

By: Eddy

<p>&nbsp;</p>

## **1. Introduction**

This document is a Developer Guide written for developers/maintainer who wish to extend or maintain the project. It is technical, and explains the inner workings of BC-TECH and how the different components of our application work together.

**Reading this Developer Guide**

| Icon | Remarks                                                                 |
|:----:|-------------------------------------------------------------------------|
|   💡  | This icon denotes useful tips to note of during development.            |
|   ❗️  | This icon denotes important details to take note of during development. |

<p></p>

The diagrams in this Developer Guide are colour coded according to the different components.

<p></p>

![diagram-legend](images/legend.png)

<p>&nbsp;</p>

## **2. Architecture**

### **2.11 Blue Wave Connection Protocol (BWCP) architecture**

![BWCP-architecture](images/BWCP-architecture.png)





## **3. Implementation**

### **3.1. Information Collector**

![diagram-information-collector](images/InformationCollectorSequenceDiagram.png)

### **3.2. Blue Wave Connection Protocol (BWCP)**

#### 3.2.1 Connection-Success

![BWCP-connection-success](images/BWCP-connection-success.png)

#### 3.2.2 Connection-Failure

![BWCP-connection-failure](images/BWCP-connection-failure.png)

#### 3.2.3 BWCP connection sequence diagram

![BWCP-connection-sequence-diagram](images/BWCP-connection-sequence-diagram.png)

#### 3.2.4 Disconnection

![BWCP-disconnection](images/BWCP-disconnection.png)









