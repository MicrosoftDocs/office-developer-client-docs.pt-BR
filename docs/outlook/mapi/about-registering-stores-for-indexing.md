---
title: Sobre o registro de armazenamentos para indexação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321823"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="241fc-103">Sobre o registro de armazenamentos para indexação</span><span class="sxs-lookup"><span data-stu-id="241fc-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="241fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="241fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="241fc-105">Este tópico é específico da Pesquisa Instantânea no Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="241fc-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="241fc-106">A Pesquisa Instantânea permite que você encontre itens rapidamente no Outlook.</span><span class="sxs-lookup"><span data-stu-id="241fc-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="241fc-107">Ele usa componentes do Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="241fc-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="241fc-108">O Manipulador de Protocolo MAPI verifica o Registro do Windows em busca de armazenamentos que ele deve indexar para fins de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="241fc-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="241fc-109">Os provedores da Loja que querem ser indexados devem ser registrados no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="241fc-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="241fc-110">Por padrão, o Windows Desktop Search adiciona os seguintes quatro tipos de provedores de loja ao Registro do Windows para permitir a indexação:</span><span class="sxs-lookup"><span data-stu-id="241fc-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="241fc-111">Armazenar arquivos de Pastas Particulares (. PST).</span><span class="sxs-lookup"><span data-stu-id="241fc-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="241fc-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span><span class="sxs-lookup"><span data-stu-id="241fc-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="241fc-113">Armazenar para pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="241fc-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="241fc-114">Store para Microsoft Office Outlook Connector para MSN.</span><span class="sxs-lookup"><span data-stu-id="241fc-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="241fc-115">Provedores de armazenamento de terceiros que querem ser indexados devem se registrar no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="241fc-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="241fc-116">Os administradores e usuários podem usar uma configuração de Política de Grupo para impedir que a Pesquisa da Área de Trabalho do Windows indexe itens do Outlook.</span><span class="sxs-lookup"><span data-stu-id="241fc-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="241fc-117">Para obter mais informações, consulte [Estendendo a Pesquisa da Área de Trabalho do Windows.](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="241fc-117">For more information, see [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="241fc-118">Chaves do Registro</span><span class="sxs-lookup"><span data-stu-id="241fc-118">Registry Keys</span></span>

<span data-ttu-id="241fc-119">Em um computador, todos os provedores de armazenamento que deseja indexar devem ser registrados em apenas uma das três chaves de registro a seguir no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="241fc-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="241fc-120">O Manipulador de Protocolo MAPI analisa cada uma dessas chaves na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="241fc-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="241fc-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span><span class="sxs-lookup"><span data-stu-id="241fc-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search</span></span>\
    
2. <span data-ttu-id="241fc-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="241fc-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
3. <span data-ttu-id="241fc-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span><span class="sxs-lookup"><span data-stu-id="241fc-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences</span></span>\
    
 <span data-ttu-id="241fc-124">Cada valor sob a chave corresponde a um provedor de armazenamento que seria indexado.</span><span class="sxs-lookup"><span data-stu-id="241fc-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="241fc-125">O nome do valor é o IDENTIFICADOr Global Exclusivo (GUID) do provedor de armazenamento, que é do tipo **DWORD** e tem o valor hexadecimal 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="241fc-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="241fc-126">GUIDs for Store Providers</span><span class="sxs-lookup"><span data-stu-id="241fc-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="241fc-127">A propriedade MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica o GUID de um armazenamento MAPI.</span><span class="sxs-lookup"><span data-stu-id="241fc-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="241fc-128">Os GUIDs para os provedores de armazenamento que os índices do Outlook estão descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="241fc-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="241fc-129">**Tipo de Provedor de Armazenamento**</span><span class="sxs-lookup"><span data-stu-id="241fc-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="241fc-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="241fc-130">**GUID**</span></span> <br/> |<span data-ttu-id="241fc-131">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="241fc-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="241fc-132">Arquivos de Pastas Particulares (. PST)</span><span class="sxs-lookup"><span data-stu-id="241fc-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="241fc-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="241fc-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="241fc-134">O GUID está documentado no arquivo de header público mspst.h **como MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="241fc-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="241fc-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="241fc-135">Exchange</span></span>  <br/> |<span data-ttu-id="241fc-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="241fc-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="241fc-137">O GUID está documentado no arquivo de cabeça público edkmdb.h como **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="241fc-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="241fc-138">Pastas públicas</span><span class="sxs-lookup"><span data-stu-id="241fc-138">Public folders</span></span>  <br/> |<span data-ttu-id="241fc-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="241fc-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="241fc-140">O GUID está documentado no arquivo de título público edkmdb.h como **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="241fc-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="241fc-141">Conector do Outlook para MSN</span><span class="sxs-lookup"><span data-stu-id="241fc-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="241fc-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="241fc-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="241fc-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="241fc-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="241fc-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="241fc-144">See also</span></span>



[<span data-ttu-id="241fc-145">Sobre a API de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="241fc-145">About the Store API</span></span>](about-the-store-api.md)

