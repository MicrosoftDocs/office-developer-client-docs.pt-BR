---
title: Método CreateObject (RDS)
TOCTitle: CreateObject method (RDS)
ms:assetid: 130debe5-31cf-4ab0-5f78-9adaec7d7126
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248905(v=office.15)
ms:contentKeyID: 48543360
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ad61495bcc96b3099af6273796626e9442cbf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295370"
---
# <a name="createobject-method-rds"></a><span data-ttu-id="1d5e9-102">Método CreateObject (RDS)</span><span class="sxs-lookup"><span data-stu-id="1d5e9-102">CreateObject method (RDS)</span></span>

<span data-ttu-id="1d5e9-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d5e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d5e9-p101">Cria o proxy para o objeto corporativo de destino e retorna um ponteiro para ele. O proxy empacota e conduz dados para o stub no servidor para comunicação com o objeto corporativo a fim de enviar solicitações e dados pela Internet. Para objetos de componente dentro do processo, nenhum proxy é utilizado, apenas é fornecido um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-p101">Creates the proxy for the target business object and returns a pointer to it. The proxy packages and marshals data to the server-side stub for communications with the business object to send requests and data over the Internet. For in-process component objects, no proxies are used, just a pointer to the object is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d5e9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d5e9-107">Syntax</span></span>

<span data-ttu-id="1d5e9-108">O Remote Data Service suporta os seguintes protocolos: HTTP, HTTPS (HTTP sobre Secure Socket Layer), DCOM e dentro do processo.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-108">Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP over Secure Socket Layer), DCOM, and in-process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d5e9-109">Protocolo</span><span class="sxs-lookup"><span data-stu-id="1d5e9-109">Protocol</span></span></p></th>
<th><p><span data-ttu-id="1d5e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d5e9-110">Syntax</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d5e9-111">HTTP</span><span class="sxs-lookup"><span data-stu-id="1d5e9-111">HTTP</span></span></p></td>
<td><p><span data-ttu-id="1d5e9-112">Definir<em></em> = <em>espaço de disco</em>de objeto. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="1d5e9-112">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d5e9-113">HTTPS</span><span class="sxs-lookup"><span data-stu-id="1d5e9-113">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="1d5e9-114">Definir<em></em> = <em>espaço de disco</em>de objeto. CreateObject (&quot;<em>ProgID</em>&quot; &quot; <em>https://awebsrvr</em>, &quot;)</span><span class="sxs-lookup"><span data-stu-id="1d5e9-114">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>https://awebsrvr</em>&quot;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d5e9-115">PROTOCOLO</span><span class="sxs-lookup"><span data-stu-id="1d5e9-115">DCOM</span></span></p></td>
<td><p><span data-ttu-id="1d5e9-116">Definir<em></em> = <em>espaço de disco</em>de objeto. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; <em>ComputerName</em>&quot;)</span><span class="sxs-lookup"><span data-stu-id="1d5e9-116">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot;<em>computername</em>&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d5e9-117">Em processo</span><span class="sxs-lookup"><span data-stu-id="1d5e9-117">In-process</span></span></p></td>
<td><p><span data-ttu-id="1d5e9-118">Definir<em></em> = <em>espaço de disco</em>de objeto. CreateObject (&quot;<em>ProgID</em>&quot;, &quot; &quot;)</span><span class="sxs-lookup"><span data-stu-id="1d5e9-118">Set<em>object</em> = <em>DataSpace</em>.CreateObject(&quot;<em>ProgId</em>&quot;, &quot; &quot;)</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="parameters"></a><span data-ttu-id="1d5e9-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d5e9-119">Parameters</span></span>

|<span data-ttu-id="1d5e9-120">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d5e9-120">Parameter</span></span>|<span data-ttu-id="1d5e9-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d5e9-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1d5e9-122">*Object*</span><span class="sxs-lookup"><span data-stu-id="1d5e9-122">*Object*</span></span> |<span data-ttu-id="1d5e9-123">Uma variável de objeto que é avaliada para um objeto que é o tipo especificado em *ProgID*.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-123">An object variable that evaluates to an object that is the type specified in *ProgID*.</span></span>|
|<span data-ttu-id="1d5e9-124">*DataSpace*</span><span class="sxs-lookup"><span data-stu-id="1d5e9-124">*DataSpace*</span></span> |<span data-ttu-id="1d5e9-125">Uma variável de objeto que representa um objeto [RDS.DataSpace](dataspace-object-rds.md) utilizado para criar uma instância do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-125">An object variable that represents an [RDS.DataSpace](dataspace-object-rds.md) object used to create an instance of the new object.</span></span>|
|<span data-ttu-id="1d5e9-126">*ProgID*</span><span class="sxs-lookup"><span data-stu-id="1d5e9-126">*ProgID*</span></span> |<span data-ttu-id="1d5e9-127">Um valor **String** que contém o identificador programático que especifica um objeto corporativo no servidor que implementa as regras comerciais de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-127">A **String** value that contains the programmatic identifier specifying a server-side business object that implements your application's business rules.</span></span>|
|<span data-ttu-id="1d5e9-128">*awebsrvr* ou *computername*</span><span class="sxs-lookup"><span data-stu-id="1d5e9-128">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="1d5e9-129">Um valor **String** que representa uma URL que identifica o servidor Web do IIS (serviços de informações da Internet) onde uma instância do objeto de negócios do servidor é criada.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-129">A **String** value that represents a URL identifying the Internet Information Services (IIS) web server where an instance of the server business object is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1d5e9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d5e9-130">Remarks</span></span>

<span data-ttu-id="1d5e9-131">O *protocolo http* é o protocolo Web padrão; *Https* é um protocolo da Web seguro.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-131">The *HTTP protocol* is the standard web protocol; *HTTPS* is a secure web protocol.</span></span> <span data-ttu-id="1d5e9-132">Utilize o *protocolo DCOM* ao executar uma rede local sem HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-132">Use the *DCOM protocol* when running a local-area network without HTTP.</span></span> <span data-ttu-id="1d5e9-133">O protocolo *dentro do processo* é uma biblioteca de vínculo dinâmico (DLL) local; ele não utiliza uma rede.</span><span class="sxs-lookup"><span data-stu-id="1d5e9-133">The *in-process* protocol is a local dynamic-link library (DLL); it does not use a network.</span></span>

