# TCP/IPの標準化


## 目次

1. [プロトコルの標準化](#プロトコルの標準化)
	1. [ISOとIETF](#isoとietf)
	1. [インターネットプロトコルスイート](#インターネットプロトコルスイート)
	1. [RFC](#rfc)
	1. [標準化の流れ](#標準化の流れ)


## プロトコルの標準化

### ISOとIETF

**ISO**（International Organization for Standardization、国際標準化機構）は、国際標準として**OSI**（Open System Interconnection）と呼ばれる通信体系を標準化した。

一方で、インターネットで使われているプロトコルである**TCP/IP**（Transmission Control Protocol / Internet Protocol）は、**IETF**（Internet Engineering Task Force）で提案・標準化作業が行われているプロトコルである。

TCP/IPは、実装することを念頭に作業が進められ、その方針から素早くプロトコルを完成させることができた。そのため、ISOのOSIよりも先に動作するプロトコルを作り上げることができ、世の中に普及していくこととなった。

### インターネットプロトコルスイート

**TCP/IP**（Transmission Control Protocol / Internet Protocol）は、TCPというプロトコルとIPというプロトコルの2つだけを指すわけではなく、これに付随したプロトコル群の総称として使われる言葉である。このプロトコル一式を、**インターネットプロトコルスイート**と呼ぶ。

### RFC

TCP/IPのプトロコルは、[IETF](#isoとietf)で議論されて標準化される。標準化しようとするプロトコルは、**RFC**（Request For Comments）と呼ばれるドキュメントとして管理されている。一度RFCになったものは、その内容を改定することはできない。そのため、同じプロトコルでも内容を更新しようとすると、新しいRFCを発行する必要がある。

RFCはプロトコルの仕様が変更されるたびに番号が変わるのが不便であるという意見もあったため、主要なプロトコルや標準に対しては、**STD**（Standard）という変化しない番号を割り振った。

また、インターネットのユーザや管理者に向けて有益な情報を提供するために、**FYI**（For Your Information）という番号付けも行われている。

[RFCのホームページ](https://www.rfc-editor.org/)

### 標準化の流れ

TCP/IPの標準化作業は、まず、仕様を煮詰める**インターネットドラフト**（I-D: Internet-Draft）から始まる。そして、標準化したほうが良いと認められるとRFCになり、**提案標準**（Proposed Standard）になる。次に標準の草案である**ドラフト標準**（Draft Standard）になり、最後に**標準**（Standard）となる。
