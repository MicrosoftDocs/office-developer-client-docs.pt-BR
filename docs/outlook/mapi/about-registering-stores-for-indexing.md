---
title: Sobre como registrar repositórios para indexação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: b16446644c360185908e7f4e58463257fe17f403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766110"
---
# <a name="about-registering-stores-for-indexing"></a><span data-ttu-id="72f6f-103">Sobre como registrar repositórios para indexação</span><span class="sxs-lookup"><span data-stu-id="72f6f-103">About Registering Stores for Indexing</span></span>

  
  
<span data-ttu-id="72f6f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72f6f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72f6f-105">Este tópico é específico para a pesquisa instantânea no Microsoft Office Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="72f6f-105">This topic is specific to Instant Search in Microsoft Office Outlook 2007.</span></span>
  
<span data-ttu-id="72f6f-106">Pesquisa instantânea permite localizar rapidamente os itens no Outlook.</span><span class="sxs-lookup"><span data-stu-id="72f6f-106">Instant Search lets you quickly find items in Outlook.</span></span> <span data-ttu-id="72f6f-107">Ele usa os componentes do Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="72f6f-107">It uses components of Windows Desktop Search.</span></span>
  
<span data-ttu-id="72f6f-108">O manipulador de protocolo MAPI verifica o registro do Windows para repositórios que ele deve indexar para fins de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="72f6f-108">The MAPI Protocol Handler checks the Windows registry for stores that it should index for search purposes.</span></span> <span data-ttu-id="72f6f-109">Provedores de armazenamento que devem ser indexados devem ser registrados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f6f-109">Store providers that want to be indexed must be registered in the Windows registry.</span></span>
  
<span data-ttu-id="72f6f-110">Por padrão, o Windows Desktop Search adiciona os seguintes quatro tipos de provedores de armazenamento no registro do Windows para permitir a indexação:</span><span class="sxs-lookup"><span data-stu-id="72f6f-110">By default, Windows Desktop Search adds the following four types of store providers to the Windows registry to allow indexing:</span></span>
  
- <span data-ttu-id="72f6f-111">Repositório de arquivos de pastas particulares (. PST).</span><span class="sxs-lookup"><span data-stu-id="72f6f-111">Store for Personal Folders files (.PST).</span></span>
    
-  <span data-ttu-id="72f6f-112">Repositório do Microsoft Exchange, incluindo quaisquer arquivos de pasta Offline (. ost).</span><span class="sxs-lookup"><span data-stu-id="72f6f-112">Microsoft Exchange store, including any Offline Folder files (.ost).</span></span> 
    
-  <span data-ttu-id="72f6f-113">Repositório para pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="72f6f-113">Store for public folders.</span></span> 
    
-  <span data-ttu-id="72f6f-114">Repositório para o Microsoft Office Outlook Connector para MSN.</span><span class="sxs-lookup"><span data-stu-id="72f6f-114">Store for Microsoft Office Outlook Connector for MSN.</span></span> 
    
 <span data-ttu-id="72f6f-115">Provedores de armazenamento de terceiros que devem ser indexados devem ser registrados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f6f-115">Third-party store providers that want to be indexed must register themselves in the Windows registry.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="72f6f-116">Os administradores e usuários podem usar uma configuração de diretiva de grupo para impedir a indexação de itens do Outlook do Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="72f6f-116">Administrators and users can use a Group Policy setting to prevent Windows Desktop Search from indexing Outlook items.</span></span> <span data-ttu-id="72f6f-117">Para obter mais informações, consulte [Estendendo o Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="72f6f-117">For more information, see [Extending Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx).</span></span> 
  
## <a name="registry-keys"></a><span data-ttu-id="72f6f-118">Chaves do registro</span><span class="sxs-lookup"><span data-stu-id="72f6f-118">Registry Keys</span></span>

<span data-ttu-id="72f6f-119">Em um computador, todos os provedores de armazenamento que devem ser indexados devem ser registrados em apenas um dos seguintes chaves de registro de três no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="72f6f-119">On a computer, all store providers that want to be indexed must be registered under only one of the following three registry keys in the Windows registry.</span></span> <span data-ttu-id="72f6f-120">O manipulador de protocolo MAPI procura sob cada uma dessas chaves na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="72f6f-120">The MAPI Protocol Handler looks under each of these keys in the following order:</span></span>
  
1. <span data-ttu-id="72f6f-121">\Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="72f6f-121">[HKLM]\Software\Policies\Microsoft\Windows\Windows Search\\</span></span>
    
2. <span data-ttu-id="72f6f-122">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]</span><span class="sxs-lookup"><span data-stu-id="72f6f-122">[HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
3. <span data-ttu-id="72f6f-123">\Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]</span><span class="sxs-lookup"><span data-stu-id="72f6f-123">[HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\\</span></span>
    
 <span data-ttu-id="72f6f-124">Cada valor na chave corresponde a um provedor de repositório que seria indexado.</span><span class="sxs-lookup"><span data-stu-id="72f6f-124">Each value under the key corresponds to a store provider that would be indexed.</span></span> <span data-ttu-id="72f6f-125">O nome do valor é o identificador global exclusivo (GUID) o provedor de armazenamento, que é do tipo **DWORD** e tem o valor hexadecimal 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="72f6f-125">The name of the value is the Globally Unique Identifier (GUID) of the store provider, which is of the type **DWORD** and has the hexadecimal value 0x00000001.</span></span> 
  
## <a name="guids-for-store-providers"></a><span data-ttu-id="72f6f-126">GUIDs de provedores de armazenamento</span><span class="sxs-lookup"><span data-stu-id="72f6f-126">GUIDs for Store Providers</span></span>

<span data-ttu-id="72f6f-127">A propriedade MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** Especifica o GUID de um repositório MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f6f-127">The MAPI property **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** specifies the GUID of a MAPI store.</span></span> <span data-ttu-id="72f6f-128">Os GUIDs para os provedores de armazenamento que os índices do Outlook estão descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="72f6f-128">The GUIDs for the store providers that Outlook indexes are described in the following table.</span></span> 
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="72f6f-129">**Tipo de provedor de armazenamento**</span><span class="sxs-lookup"><span data-stu-id="72f6f-129">**Type of Store Provider**</span></span> <br/> |<span data-ttu-id="72f6f-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="72f6f-130">**GUID**</span></span> <br/> |<span data-ttu-id="72f6f-131">**Notes**</span><span class="sxs-lookup"><span data-stu-id="72f6f-131">**Notes**</span></span> <br/> |
|<span data-ttu-id="72f6f-132">Arquivos de pastas particulares (. PST)</span><span class="sxs-lookup"><span data-stu-id="72f6f-132">Personal Folders files (.PST)</span></span>  <br/> |<span data-ttu-id="72f6f-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span><span class="sxs-lookup"><span data-stu-id="72f6f-133">{4154494E-BFF9-01B8-00AA-0037D96E0000}</span></span>  <br/> |<span data-ttu-id="72f6f-134">GUID documentada a mspst.h do arquivo de cabeçalho público como **MSPST_UID_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="72f6f-134">GUID is documented in the public header file mspst.h as **MSPST_UID_PROVIDER**</span></span> <br/> |
|<span data-ttu-id="72f6f-135">Exchange</span><span class="sxs-lookup"><span data-stu-id="72f6f-135">Exchange</span></span>  <br/> |<span data-ttu-id="72f6f-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span><span class="sxs-lookup"><span data-stu-id="72f6f-136">{C0A19454-7F29-1B10-A587-08002B2A2517}</span></span>  <br/> |<span data-ttu-id="72f6f-137">GUID documentada o arquivo de cabeçalho público Edkmdb. h como **pbExchangeProviderPrimaryUserGuid**</span><span class="sxs-lookup"><span data-stu-id="72f6f-137">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPrimaryUserGuid**</span></span> <br/> |
|<span data-ttu-id="72f6f-138">Pastas públicas</span><span class="sxs-lookup"><span data-stu-id="72f6f-138">Public folders</span></span>  <br/> |<span data-ttu-id="72f6f-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span><span class="sxs-lookup"><span data-stu-id="72f6f-139">{70fab278-f7af-cd11-9bc8-00aa002fc45a}</span></span>  <br/> |<span data-ttu-id="72f6f-140">GUID documentada o arquivo de cabeçalho público Edkmdb. h como **pbExchangeProviderPublicGuid**</span><span class="sxs-lookup"><span data-stu-id="72f6f-140">GUID is documented in the public header file edkmdb.h as **pbExchangeProviderPublicGuid**</span></span> <br/> |
|<span data-ttu-id="72f6f-141">O Outlook Connector para MSN</span><span class="sxs-lookup"><span data-stu-id="72f6f-141">Outlook Connector for MSN</span></span>  <br/> |<span data-ttu-id="72f6f-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span><span class="sxs-lookup"><span data-stu-id="72f6f-142">{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}</span></span>  <br/> |<span data-ttu-id="72f6f-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="72f6f-143">None</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72f6f-144">Ver também</span><span class="sxs-lookup"><span data-stu-id="72f6f-144">See also</span></span>



[<span data-ttu-id="72f6f-145">Sobre o API de armazenamento</span><span class="sxs-lookup"><span data-stu-id="72f6f-145">About the Store API</span></span>](about-the-store-api.md)

