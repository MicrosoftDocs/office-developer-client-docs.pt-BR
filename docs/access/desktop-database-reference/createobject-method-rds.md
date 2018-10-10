---
title: Método CreateObject (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2d1e3cc0128f4490105b24d7181119f6fece9b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462882"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="319b7-102">Método CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="319b7-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="319b7-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="319b7-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="319b7-p101">Cria o proxy para o objeto corporativo de destino e retorna um ponteiro para ele. O proxy empacota e conduz dados para o stub no servidor para comunicação com o objeto corporativo a fim de enviar solicitações e dados pela Internet. Para objetos de componente dentro do processo, nenhum proxy é utilizado, apenas é fornecido um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="319b7-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="319b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="319b7-107">Syntax</span></span>

<span data-ttu-id="319b7-108">O Remote Data Service suporta os seguintes protocolos: HTTP, HTTPS (HTTP sobre Secure Socket Layer), DCOM e dentro do processo.</span><span class="sxs-lookup"><span data-stu-id="319b7-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="319b7-109">Protocolo</span><span class="sxs-lookup"><span data-stu-id="319b7-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="319b7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="319b7-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="319b7-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="319b7-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="319b7-112">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="319b7-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="319b7-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="319b7-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="319b7-114">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="319b7-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="319b7-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="319b7-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="319b7-116">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="319b7-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="319b7-117">Em processo</span><span class="sxs-lookup"><span data-stu-id="319b7-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="319b7-118">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="319b7-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="319b7-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="319b7-119">Parameters</span></span>

  - <span data-ttu-id="319b7-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="319b7-120">*Object*</span></span>

  - <span data-ttu-id="319b7-121">Uma variável de objeto que é avaliada para um objeto que é o tipo especificado em *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="319b7-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="319b7-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="319b7-122">*DataSpace*</span></span>

  - <span data-ttu-id="319b7-123">Uma variável de objeto que representa um objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para criar uma instância do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="319b7-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="319b7-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="319b7-124">*ProgID*</span></span>

  - <span data-ttu-id="319b7-125">Um valor **String** que contém o identificador programático que especifica um objeto corporativo no servidor que implementa as regras comerciais de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="319b7-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="319b7-126">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="319b7-126">*awebsrvr* or *computername*</span></span>

  - <span data-ttu-id="319b7-127">Um valor **String** que representa uma URL que identifica o servidor Web do Internet Information Services (IIS) em que uma instância do objeto corporativo do servidor é criada.</span><span class="sxs-lookup"><span data-stu-id="319b7-127">A **String** value that represents a URL identifying the Internet Information Services (IIS) Web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="319b7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="319b7-128">Remarks</span></span>

<span data-ttu-id="319b7-129">O *protocolo HTTP* é o protocolo padrão da Web; *HTTPS* é um protocolo da Web seguro.</span><span class="sxs-lookup"><span data-stu-id="319b7-129">The *HTTP protocol* is the standard Web protocol; *HTTPS* is a secure Web protocol.</span></span> <span data-ttu-id="319b7-130">Use o *protocolo DCOM* durante a execução de uma rede de área local sem HTTP.</span><span class="sxs-lookup"><span data-stu-id="319b7-130">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="319b7-131">O protocolo de *em processo* é uma biblioteca de vínculo dinâmico (DLL); local ele não usa uma rede.</span><span class="sxs-lookup"><span data-stu-id="319b7-131">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

