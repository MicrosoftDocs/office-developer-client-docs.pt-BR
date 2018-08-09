---
title: Propriedade canônica PidTagFolderWebViewInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 62bc0e75d0a405ebe9f68ec9f4af1ca038bda219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769269"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="26631-103">Propriedade canônica PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="26631-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="26631-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26631-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26631-105">Contém a URL da home page de uma pasta no Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="26631-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="26631-106">Essa propriedade contém um fluxo binário chamado **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="26631-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26631-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="26631-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="26631-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="26631-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="26631-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="26631-109">Identifier:</span></span>  <br/> |<span data-ttu-id="26631-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="26631-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="26631-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="26631-111">Data type:</span></span>  <br/> |<span data-ttu-id="26631-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="26631-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="26631-113">Área:</span><span class="sxs-lookup"><span data-stu-id="26631-113">Area:</span></span>  <br/> |<span data-ttu-id="26631-114">Pasta MAPI</span><span class="sxs-lookup"><span data-stu-id="26631-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26631-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="26631-115">Remarks</span></span>

<span data-ttu-id="26631-116">Uma URL da home page pode ser especificada para qualquer pasta do Outlook.</span><span class="sxs-lookup"><span data-stu-id="26631-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="26631-117">Essas informações podem ser acessadas no Outlook a partir da guia **página inicial** da caixa de diálogo Propriedades de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="26631-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="26631-118">Dependendo de determinadas configurações de diretiva, a home page pode ser ignorada pelo Outlook se o repositório MAPI que contém essa pasta não relata MSCAP_SECURE_FOLDER_HOMEPAGES em sua implementação [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="26631-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="26631-119">**A pasta** e uma pasta pública podem ter URLs de home page.</span><span class="sxs-lookup"><span data-stu-id="26631-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="26631-120">No entanto **a pasta** usa um mecanismo diferente para gerenciar sua URL da home page; Esse mecanismo não é abordado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="26631-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="26631-121">Uma pasta pública também pode ter uma URL da home page definido dentro dela que é específico para um usuário.</span><span class="sxs-lookup"><span data-stu-id="26631-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="26631-122">No entanto, esse recurso não está descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="26631-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="26631-123">O valor dessa propriedade é um fluxo binário chamado **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="26631-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="26631-124">Estrutura de fluxo de WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="26631-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="26631-125">A estrutura de fluxo de **WebViewPersistenceObject** contém informações sobre uma URL da home page de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="26631-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="26631-126">Elementos de dados nesta estrutura são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="26631-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="26631-127">A seguinte descrição pode não listar todos os valores de campo suportados pelo Outlook; Portanto, quando seu código lê um stream existente, alguns sinalizadores que não estão listados aqui podem também ser encontrados.</span><span class="sxs-lookup"><span data-stu-id="26631-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="26631-128">No entanto, você pode usar essa descrição criar programaticamente os valores da propriedade **PidTagFolderWebViewInfo** que o Outlook compreenderá.</span><span class="sxs-lookup"><span data-stu-id="26631-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="26631-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="26631-129">_dwVersion_</span></span>
  
> <span data-ttu-id="26631-130">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="26631-130">DWORD (4 bytes).</span></span> <span data-ttu-id="26631-131">A versão do formato da estrutura.</span><span class="sxs-lookup"><span data-stu-id="26631-131">The version of the structure's format.</span></span> <span data-ttu-id="26631-132">A partir do Microsoft Office Outlook 2007, o único valor com suporte para este campo é da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="26631-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="26631-133">**Value name**</span><span class="sxs-lookup"><span data-stu-id="26631-133">**Value name**</span></span>|<span data-ttu-id="26631-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26631-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26631-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="26631-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="26631-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="26631-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="26631-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="26631-137">_dwType_</span></span>
  
> <span data-ttu-id="26631-138">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="26631-138">DWORD (4 bytes).</span></span> <span data-ttu-id="26631-139">O tipo de informações da página inicial.</span><span class="sxs-lookup"><span data-stu-id="26631-139">The type of the home page information.</span></span> <span data-ttu-id="26631-140">A partir do Microsoft Office Outlook 2007, o único valor com suporte para este campo é da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="26631-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="26631-141">**Value name**</span><span class="sxs-lookup"><span data-stu-id="26631-141">**Value name**</span></span>|<span data-ttu-id="26631-142">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26631-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26631-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="26631-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="26631-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="26631-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="26631-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="26631-145">_dwFlags_</span></span>
  
> <span data-ttu-id="26631-146">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="26631-146">DWORD (4 bytes).</span></span> <span data-ttu-id="26631-147">Uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="26631-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="26631-148">Sinalizador nome \* \* \*</span><span class="sxs-lookup"><span data-stu-id="26631-148">****Flag name****</span></span>|<span data-ttu-id="26631-149">****Valor****</span><span class="sxs-lookup"><span data-stu-id="26631-149">****Value****</span></span>|<span data-ttu-id="26631-150">****Descrição****</span><span class="sxs-lookup"><span data-stu-id="26631-150">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26631-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="26631-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="26631-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="26631-152">0x00000001</span></span>  <br/> |<span data-ttu-id="26631-153">A caixa de seleção **Mostrar home page por padrão para esta pasta** foi verificada na guia **página inicial** da caixa de diálogo Propriedades de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="26631-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="26631-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="26631-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="26631-155">Uma matriz de elementos DWORD 7 (total de 28 bytes).</span><span class="sxs-lookup"><span data-stu-id="26631-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="26631-156">Unused.</span><span class="sxs-lookup"><span data-stu-id="26631-156">Unused.</span></span>
    
<span data-ttu-id="26631-157">cbData diferente</span><span class="sxs-lookup"><span data-stu-id="26631-157">cbData</span></span>
  
> <span data-ttu-id="26631-158">Um ULONG (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="26631-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="26631-159">O tamanho, em bytes, do elemento de dados _wzURL_ .</span><span class="sxs-lookup"><span data-stu-id="26631-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="26631-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="26631-160">_wzURL_</span></span>
  
> <span data-ttu-id="26631-161">Uma matriz de elementos WCHAR.</span><span class="sxs-lookup"><span data-stu-id="26631-161">An array of WCHAR elements.</span></span> <span data-ttu-id="26631-162">A representação UTF-16 da cadeia de caracteres de URL HomePage terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="26631-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="26631-163">Exemplo de fluxo de WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="26631-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="26631-164">Esta seção descreve um exemplo de um fluxo de **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="26631-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="26631-165">O fluxo Especifica a URL da home page "http://www.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="26631-165">The stream specifies the home page URL "http://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="26631-166">**Despejo de dados**</span><span class="sxs-lookup"><span data-stu-id="26631-166">**Data dump**</span></span>
  
<span data-ttu-id="26631-167">A seguir está um despejo do fluxo de dados como ela seria exibida em um editor de binário.</span><span class="sxs-lookup"><span data-stu-id="26631-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="26631-168">**Deslocamento de fluxo**</span><span class="sxs-lookup"><span data-stu-id="26631-168">**Stream offset**</span></span>|<span data-ttu-id="26631-169">**Bytes de dados**</span><span class="sxs-lookup"><span data-stu-id="26631-169">**Data bytes**</span></span>|<span data-ttu-id="26631-170">**Dados ASCII**</span><span class="sxs-lookup"><span data-stu-id="26631-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26631-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="26631-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="26631-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="26631-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="26631-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="26631-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="26631-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="26631-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="26631-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="26631-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="26631-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="26631-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="26631-177">A seguir está uma análise dos dados de amostra para o fluxo de **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="26631-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="26631-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="26631-178">_dwVersion_</span></span>
  
> <span data-ttu-id="26631-179">Deslocamento 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="26631-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="26631-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="26631-180">_dwType_</span></span>
  
> <span data-ttu-id="26631-181">Deslocamento 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="26631-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="26631-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="26631-182">_dwFlags_</span></span>
  
> <span data-ttu-id="26631-183">Deslocamento 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="26631-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="26631-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="26631-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="26631-185">Deslocamento 0xC, 28 bytes: zeros.</span><span class="sxs-lookup"><span data-stu-id="26631-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="26631-186">_cbData diferente_</span><span class="sxs-lookup"><span data-stu-id="26631-186">_cbData_</span></span>
  
> <span data-ttu-id="26631-187">Deslocamento 0x28, 4 bytes: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="26631-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="26631-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="26631-188">_wzURL_</span></span>
  
> <span data-ttu-id="26631-189">Deslocamento 0x2C, 0x32 bytes: matriz de 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="26631-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="26631-190">Um valor de cadeia de caracteres terminada em zero Unicode: "http://www.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="26631-190">A Unicode zero-terminated string value: "http://www.microsoft.com".</span></span>
    

