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
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316307"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="8882b-103">Propriedade canônica PidTagFolderWebViewInfo</span><span class="sxs-lookup"><span data-stu-id="8882b-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="8882b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8882b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8882b-105">Contém a URL da Home Page de uma pasta no Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="8882b-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="8882b-106">Esta propriedade contém um fluxo binário chamado **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="8882b-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8882b-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8882b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8882b-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="8882b-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="8882b-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8882b-109">Identifier:</span></span>  <br/> |<span data-ttu-id="8882b-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="8882b-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="8882b-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8882b-111">Data type:</span></span>  <br/> |<span data-ttu-id="8882b-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8882b-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8882b-113">Área:</span><span class="sxs-lookup"><span data-stu-id="8882b-113">Area:</span></span>  <br/> |<span data-ttu-id="8882b-114">Pasta MAPI</span><span class="sxs-lookup"><span data-stu-id="8882b-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8882b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8882b-115">Remarks</span></span>

<span data-ttu-id="8882b-116">Uma URL de página inicial pode ser especificada para qualquer pasta do Outlook.</span><span class="sxs-lookup"><span data-stu-id="8882b-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="8882b-117">Essas informações podem ser acessadas no Outlook na guia **página inicial** da caixa de diálogo Propriedades de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="8882b-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="8882b-118">Dependendo de determinadas configurações de política, a Home Page poderá ser ignorada pelo Outlook se o repositório MAPI que contém essa pasta não relatar MSCAP_SECURE_FOLDER_HOMEPAGES em sua implementação do [IMSCapabilities:: GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8882b-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="8882b-119">A pasta **Outlook hoje** e uma pasta pública podem ter URLs de Home Page.</span><span class="sxs-lookup"><span data-stu-id="8882b-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="8882b-120">No enTanto, a pasta **Outlook hoje** usa um mecanismo diferente para gerenciar a URL da Home Page; Esse mecanismo não é abordado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8882b-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="8882b-121">Uma pasta pública também pode ter uma URL de home page definida no que é específica de um usuário.</span><span class="sxs-lookup"><span data-stu-id="8882b-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="8882b-122">No enTanto, esse recurso não é descrito neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8882b-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="8882b-123">O valor dessa propriedade é um fluxo binário chamado **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="8882b-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="8882b-124">Estrutura de fluxo WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="8882b-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="8882b-125">A estrutura de fluxo **WebViewPersistenceObject** contém informações sobre uma URL de página inicial de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="8882b-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="8882b-126">Os elementos de dados nessa estrutura são armazenados em uma ordem de byte little-endian, imediatamente após um outro na seguinte ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="8882b-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8882b-127">A descrição a seguir pode não listar todos os valores de campo suportados pelo Outlook; Portanto, quando o código lê um fluxo existente, alguns sinalizadores que não estão listados aqui também podem ser encontrados.</span><span class="sxs-lookup"><span data-stu-id="8882b-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="8882b-128">No enTanto, você pode usar essa descrição para criar programaticamente valores para a propriedade **PidTagFolderWebViewInfo** que o Outlook entenderá.</span><span class="sxs-lookup"><span data-stu-id="8882b-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="8882b-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="8882b-129">_dwVersion_</span></span>
  
> <span data-ttu-id="8882b-130">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="8882b-130">DWORD (4 bytes).</span></span> <span data-ttu-id="8882b-131">A versão do formato da estrutura.</span><span class="sxs-lookup"><span data-stu-id="8882b-131">The version of the structure's format.</span></span> <span data-ttu-id="8882b-132">A partir do Microsoft Office Outlook 2007, o único valor com suporte para esse campo é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="8882b-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="8882b-133">**Value name**</span><span class="sxs-lookup"><span data-stu-id="8882b-133">**Value name**</span></span>|<span data-ttu-id="8882b-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8882b-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8882b-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="8882b-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="8882b-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8882b-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="8882b-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="8882b-137">_dwType_</span></span>
  
> <span data-ttu-id="8882b-138">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="8882b-138">DWORD (4 bytes).</span></span> <span data-ttu-id="8882b-139">O tipo das informações da Home Page.</span><span class="sxs-lookup"><span data-stu-id="8882b-139">The type of the home page information.</span></span> <span data-ttu-id="8882b-140">A partir do Microsoft Office Outlook 2007, o único valor com suporte para esse campo é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="8882b-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="8882b-141">**Value name**</span><span class="sxs-lookup"><span data-stu-id="8882b-141">**Value name**</span></span>|<span data-ttu-id="8882b-142">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8882b-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8882b-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="8882b-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="8882b-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8882b-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="8882b-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8882b-145">_dwFlags_</span></span>
  
> <span data-ttu-id="8882b-146">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="8882b-146">DWORD (4 bytes).</span></span> <span data-ttu-id="8882b-147">Uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8882b-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="8882b-148">Nome do sinalizador \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8882b-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="8882b-149">\*\*\*\*Valor\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8882b-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="8882b-150">\*\*\*\*Descrição\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8882b-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8882b-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="8882b-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="8882b-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8882b-152">0x00000001</span></span>  <br/> |<span data-ttu-id="8882b-153">A caixa de seleção **mostrar página inicial por padrão para esta pasta** foi selecionada na guia **página inicial** da caixa de diálogo Propriedades de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="8882b-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="8882b-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="8882b-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="8882b-155">Uma matriz de sete elementos DWORD (total de 28 bytes).</span><span class="sxs-lookup"><span data-stu-id="8882b-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="8882b-156">Não usados.</span><span class="sxs-lookup"><span data-stu-id="8882b-156">Unused.</span></span>
    
<span data-ttu-id="8882b-157">cbData</span><span class="sxs-lookup"><span data-stu-id="8882b-157">cbData</span></span>
  
> <span data-ttu-id="8882b-158">Um ULONG (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="8882b-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="8882b-159">O tamanho, em bytes, do elemento de dados _wzURL_ .</span><span class="sxs-lookup"><span data-stu-id="8882b-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="8882b-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="8882b-160">_wzURL_</span></span>
  
> <span data-ttu-id="8882b-161">Uma matriz de elementos WCHAR.</span><span class="sxs-lookup"><span data-stu-id="8882b-161">An array of WCHAR elements.</span></span> <span data-ttu-id="8882b-162">A representação UTF-16 da cadeia de URL da Home Page terminada em zero.</span><span class="sxs-lookup"><span data-stu-id="8882b-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="8882b-163">Exemplo de fluxo WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="8882b-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="8882b-164">Esta seção descreve um exemplo de um fluxo do **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="8882b-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="8882b-165">O Stream especifica a URL da Home Pagehttps://www.microsoft.com"".</span><span class="sxs-lookup"><span data-stu-id="8882b-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="8882b-166">**Despejo de dados**</span><span class="sxs-lookup"><span data-stu-id="8882b-166">**Data dump**</span></span>
  
<span data-ttu-id="8882b-167">O seguinte é um despejo de dados do Stream como seria exibido em um editor binário.</span><span class="sxs-lookup"><span data-stu-id="8882b-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="8882b-168">**Deslocamento de fluxo**</span><span class="sxs-lookup"><span data-stu-id="8882b-168">**Stream offset**</span></span>|<span data-ttu-id="8882b-169">**Bytes de dados**</span><span class="sxs-lookup"><span data-stu-id="8882b-169">**Data bytes**</span></span>|<span data-ttu-id="8882b-170">**Dados ASCII**</span><span class="sxs-lookup"><span data-stu-id="8882b-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8882b-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="8882b-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="8882b-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="8882b-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="8882b-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="8882b-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="8882b-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="8882b-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="8882b-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="8882b-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="8882b-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="8882b-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="8882b-177">Veja a seguir uma análise dos dados de exemplo para o fluxo do **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="8882b-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="8882b-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="8882b-178">_dwVersion_</span></span>
  
> <span data-ttu-id="8882b-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="8882b-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="8882b-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="8882b-180">_dwType_</span></span>
  
> <span data-ttu-id="8882b-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="8882b-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="8882b-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8882b-182">_dwFlags_</span></span>
  
> <span data-ttu-id="8882b-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="8882b-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="8882b-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="8882b-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="8882b-185">Offset 0xC, 28 bytes: todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="8882b-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="8882b-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="8882b-186">_cbData_</span></span>
  
> <span data-ttu-id="8882b-187">Offset 0x28, 4 bytes: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="8882b-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="8882b-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="8882b-188">_wzURL_</span></span>
  
> <span data-ttu-id="8882b-189">Offset 0x2C, 0x32 bytes: matriz de 25 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="8882b-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="8882b-190">Um valor de cadeia de caracteres Unicode terminadahttps://www.microsoft.comem zero: "".</span><span class="sxs-lookup"><span data-stu-id="8882b-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

