---
title: Método CreateObject (RDS)
TOCTitle: CreateObject Method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 87bba22a6563c92e78b5dff3f737c0963de51cb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867388"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="1fac8-102">Método CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="1fac8-102">CreateObject Method (RDS)</span></span>


<span data-ttu-id="1fac8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fac8-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1fac8-p101">Cria o proxy para o objeto corporativo de destino e retorna um ponteiro para ele. O proxy empacota e conduz dados para o stub no servidor para comunicação com o objeto corporativo a fim de enviar solicitações e dados pela Internet. Para objetos de componente dentro do processo, nenhum proxy é utilizado, apenas é fornecido um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1fac8-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fac8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fac8-107">Syntax</span></span>

<span data-ttu-id="1fac8-108">O Remote Data Service suporta os seguintes protocolos: HTTP, HTTPS (HTTP sobre Secure Socket Layer), DCOM e dentro do processo.</span><span class="sxs-lookup"><span data-stu-id="1fac8-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fac8-109">Protocolo</span><span class="sxs-lookup"><span data-stu-id="1fac8-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="1fac8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fac8-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fac8-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="1fac8-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="1fac8-112">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="1fac8-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fac8-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="1fac8-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="1fac8-114">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>https://awebsrvr</em> &quot;)</span><span class="sxs-lookup"><span data-stu-id="1fac8-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fac8-115">DCOM</span><span class="sxs-lookup"><span data-stu-id="1fac8-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="1fac8-116">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; <em>computername</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="1fac8-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fac8-117">Em processo</span><span class="sxs-lookup"><span data-stu-id="1fac8-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="1fac8-118">Definir o<em>objeto</em> = <em>DataSpace</em>. CreateObject (&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="1fac8-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="1fac8-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fac8-119">Parameters</span></span>

  - <span data-ttu-id="1fac8-120">*Object*</span><span class="sxs-lookup"><span data-stu-id="1fac8-120">*Object*</span></span>

  - <span data-ttu-id="1fac8-121">Uma variável de objeto que é avaliada para um objeto que é o tipo especificado em *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="1fac8-121">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>

  - <span data-ttu-id="1fac8-122">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="1fac8-122">*DataSpace*</span></span>

  - <span data-ttu-id="1fac8-123">Uma variável de objeto que representa um objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para criar uma instância do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="1fac8-123">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>

  - <span data-ttu-id="1fac8-124">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="1fac8-124">*ProgID*</span></span>

  - <span data-ttu-id="1fac8-125">Um valor **String** que contém o identificador programático que especifica um objeto corporativo no servidor que implementa as regras comerciais de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fac8-125">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>

  - <span data-ttu-id="1fac8-126">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="1fac8-126">*awebsrvr* or *computername*</span></span>

  - <span data-ttu-id="1fac8-127">Um valor **String** que representa uma URL que identifica o servidor de web de serviços de informações da Internet (IIS) em que uma instância do objeto de negócios do servidor é criado.</span><span class="sxs-lookup"><span data-stu-id="1fac8-127">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fac8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fac8-128">Remarks</span></span>

<span data-ttu-id="1fac8-129">O *protocolo HTTP* é o protocolo padrão da web; *HTTPS* é um protocolo da web seguro.</span><span class="sxs-lookup"><span data-stu-id="1fac8-129">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="1fac8-130">Use o *protocolo DCOM* durante a execução de uma rede de área local sem HTTP.</span><span class="sxs-lookup"><span data-stu-id="1fac8-130">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="1fac8-131">O protocolo de *em processo* é uma biblioteca de vínculo dinâmico (DLL); local ele não usa uma rede.</span><span class="sxs-lookup"><span data-stu-id="1fac8-131">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

