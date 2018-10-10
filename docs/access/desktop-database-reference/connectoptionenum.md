---
title: ConnectOptionEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectOptionEnum
ms:assetid: 803d3fd6-93cf-85ea-eeb0-ca1bc965577d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249544(v=office.15)
ms:contentKeyID: 48545921
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e2e8439099732cd3e1e9aa7531f5ae3be25d7ebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462304"
---
# <a name="connectoptionenum"></a><span data-ttu-id="c349c-102">ConnectOptionEnum</span><span class="sxs-lookup"><span data-stu-id="c349c-102">ConnectOptionEnum</span></span>


<span data-ttu-id="c349c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c349c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c349c-104">Especifica se o método [Open](open-method-ado-connection.md) de um objeto [Connection](connection-object-ado.md) deve ser retornado após a conexão (de maneira síncrona) ou antes da (de maneira assíncrona) conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="c349c-104">Specifies whether the [Open](open-method-ado-connection.md) method of a [Connection](connection-object-ado.md) object should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c349c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="c349c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c349c-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c349c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c349c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c349c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c349c-108"><strong>opção adAsyncConnect</strong></span><span class="sxs-lookup"><span data-stu-id="c349c-108"><strong>adAsyncConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="c349c-109">16</span><span class="sxs-lookup"><span data-stu-id="c349c-109">16</span></span></p></td>
<td><p><span data-ttu-id="c349c-p101">Abre a conexão de maneira assíncrona. O evento <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> pode ser usado para determinar quando a conexão está disponível.</span><span class="sxs-lookup"><span data-stu-id="c349c-p101">Opens the connection asynchronously. The <a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a> event may be used to determine when the connection is available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c349c-112"><strong>adConnectUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="c349c-112"><strong>adConnectUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="c349c-113">-1</span><span class="sxs-lookup"><span data-stu-id="c349c-113">-1</span></span></p></td>
<td><p><span data-ttu-id="c349c-p102">Padrão. Abre a conexão de maneira síncrona.</span><span class="sxs-lookup"><span data-stu-id="c349c-p102">Default. Opens the connection synchronously.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c349c-116">**ADO/WFC Equivalente**</span><span class="sxs-lookup"><span data-stu-id="c349c-116">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c349c-117">Pacote: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c349c-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c349c-118">Constante</span><span class="sxs-lookup"><span data-stu-id="c349c-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c349c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span><span class="sxs-lookup"><span data-stu-id="c349c-119">AdoEnums.ConnectOption.ASYNCCONNECT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c349c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="c349c-120">AdoEnums.ConnectOption.CONNECTUNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

