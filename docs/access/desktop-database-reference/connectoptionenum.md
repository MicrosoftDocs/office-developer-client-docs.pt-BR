---
title: ConnectOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 37420ab37b350f0f852305958edbf414d9aecdb3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867311"
---
# <a name="connectoptionenum"></a><span data-ttu-id="4d62c-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="4d62c-102">ConnectOptionEnum</span></span>

<span data-ttu-id="4d62c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d62c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d62c-104">Especifica se o método [Open](open-method-ado-connection.md) de um objeto [Connection](connection-object-ado.md) deve ser retornado após a conexão (de maneira síncrona) ou antes da (de maneira assíncrona) conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="4d62c-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d62c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="4d62c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4d62c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="4d62c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4d62c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d62c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d62c-108"><strong>opção adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="4d62c-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="4d62c-109">16</span><span class="sxs-lookup"><span data-stu-id="4d62c-109">16</span></span></p></td>
<td><p><span data-ttu-id="4d62c-p101">Abre a conexão de maneira assíncrona. O evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> pode ser usado para determinar quando a conexão está disponível.</span><span class="sxs-lookup"><span data-stu-id="4d62c-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d62c-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="4d62c-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="4d62c-113">-1</span><span class="sxs-lookup"><span data-stu-id="4d62c-113">-1</span></span></p></td>
<td><p><span data-ttu-id="4d62c-p102">Padrão. Abre a conexão de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="4d62c-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4d62c-116">Equivalente ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4d62c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="4d62c-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4d62c-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4d62c-118">Constante</span><span class="sxs-lookup"><span data-stu-id="4d62c-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d62c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="4d62c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d62c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="4d62c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

