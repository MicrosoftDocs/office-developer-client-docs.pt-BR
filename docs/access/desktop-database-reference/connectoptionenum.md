---
title: ConnectOptionEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95b622d2216b085ffd0f76c8a26533187c17bd7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295678"
---
# <a name="connectoptionenum"></a><span data-ttu-id="d7100-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="d7100-102">ConnectOptionEnum</span></span>

<span data-ttu-id="d7100-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7100-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7100-104">Especifica se o método [Open](open-method-ado-connection.md) de um objeto [Connection](connection-object-ado.md) deve ser retornado após a conexão (de maneira síncrona) ou antes da (de maneira assíncrona) conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="d7100-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7100-105">Constant</span><span class="sxs-lookup"><span data-stu-id="d7100-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="d7100-106">Valor</span><span class="sxs-lookup"><span data-stu-id="d7100-106">Value</span></span></p></th>
<th><p><span data-ttu-id="d7100-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7100-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7100-108"><strong>Opção adasyncconnect</strong></span><span class="sxs-lookup"><span data-stu-id="d7100-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="d7100-109">dezesseis</span><span class="sxs-lookup"><span data-stu-id="d7100-109">16</span></span></p></td>
<td><p><span data-ttu-id="d7100-p101">Abre a conexão de maneira assíncrona. O evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> pode ser usado para determinar quando a conexão está disponível.</span><span class="sxs-lookup"><span data-stu-id="d7100-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7100-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="d7100-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="d7100-113">-1</span><span class="sxs-lookup"><span data-stu-id="d7100-113">-1</span></span></p></td>
<td><p><span data-ttu-id="d7100-p102">Padrão. Abre a conexão de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="d7100-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="d7100-116">Equivalente do ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="d7100-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="d7100-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="d7100-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d7100-118">Constant</span><span class="sxs-lookup"><span data-stu-id="d7100-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7100-119">AdoEnums. ConnectOption. ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="d7100-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7100-120">AdoEnums. ConnectOption. CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="d7100-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

