---
title: Entradas de propriedade nas seções do serviço de mensagens MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427994"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="439e3-103">Entradas de propriedade nas seções do serviço de mensagens MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="439e3-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="439e3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="439e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="439e3-105">Entradas que definem propriedades usam este formato:</span><span class="sxs-lookup"><span data-stu-id="439e3-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="439e3-106">**marca de propriedade** **=** valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="439e3-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="439e3-107">A marca de propriedade pode ser uma marca de propriedade MAPI padrão se os dados de configuração representarem uma das propriedades predefinidas por MAPI ou uma marca não padrão se os dados não representarem uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="439e3-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="439e3-108">A marca não padrão é feita combinando o valor de um identificador de propriedade com um tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="439e3-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="439e3-109">O resultado é um número hexadecimal de 8 dígitos.</span><span class="sxs-lookup"><span data-stu-id="439e3-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="439e3-110">O valor da propriedade pode ser o que fizer sentido para a marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="439e3-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="439e3-111">As seções do serviço de mensagens podem conter diversas entradas, dependendo do serviço de mensagens que está sendo configurado.</span><span class="sxs-lookup"><span data-stu-id="439e3-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="439e3-112">As propriedades MAPI a seguir geralmente estão incluídas em uma seção de serviços de mensagens no formato listado:</span><span class="sxs-lookup"><span data-stu-id="439e3-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="439e3-113">\*\*\*\* =  _Cadeia de caracteres_ PR_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="439e3-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="439e3-114">**PR_SERVICE_DLL_NAME** =  _nome do arquivo dll_</span><span class="sxs-lookup"><span data-stu-id="439e3-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="439e3-115">**PR_SERVICE_ENTRY_NAME** =  _nome da função de ponto de entrada_</span><span class="sxs-lookup"><span data-stu-id="439e3-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="439e3-116">**PR_SERVICE_SUPPORT_FILES** =  _lista de arquivos_</span><span class="sxs-lookup"><span data-stu-id="439e3-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="439e3-117">**PR_SERVICE_DELETE_FILES** =  _lista de arquivos_</span><span class="sxs-lookup"><span data-stu-id="439e3-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="439e3-118">\*\*\*\* =  _Bitmask_ PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="439e3-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="439e3-119">A cadeia de caracteres **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o nome do serviço de mensagens que é mostrado na interface do usuário, o nome que o usuário associa ao serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="439e3-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="439e3-120">O nome para exibição é uma entrada opcional no MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="439e3-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="439e3-121">Às vezes, o nome de exibição será composto de duas partes; uma parte atribuída pelo serviço de mensagens e uma parte atribuída pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="439e3-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="439e3-122">Se o usuário for responsável por atribuir uma das partes, isso geralmente é tratado com uma caixa de diálogo especial conhecida como folha de propriedades fornecida pelo serviço de mensagens sob o controle de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="439e3-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="439e3-123">As informações fornecidas para a entrada **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) é o nome da dll que contém o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="439e3-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="439e3-124">As informações fornecidas para a entrada **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) é o nome da função de ponto de entrada dentro dessa DLL que MAPI chama para configurar o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="439e3-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="439e3-125">Os arquivos listados na entrada **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) são arquivos que devem ser instalados com o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="439e3-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="439e3-126">Da mesma forma, os arquivos na entrada **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) devem ser removidos quando o serviço de mensagens é removido.</span><span class="sxs-lookup"><span data-stu-id="439e3-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="439e3-127">A entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) é uma coleção de opções definidas para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="439e3-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="439e3-128">Por exemplo, o bit SERVICE_SINGLE_COPY é definido quando o serviço de mensagens só pode aparecer uma vez em um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="439e3-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="439e3-129">O bit SERVICE_NO_PRIMARY_IDENTITY é definido se o serviço de mensagens não fornecer informações de identidade.</span><span class="sxs-lookup"><span data-stu-id="439e3-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="439e3-130">Seguem dois exemplos de entradas de propriedade não padrão.</span><span class="sxs-lookup"><span data-stu-id="439e3-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="439e3-131">A primeira entrada especifica o caminho para o arquivo usado pelo catálogo de endereços padrão como o valor da propriedade; a segunda entrada especifica um valor de propriedade numérica.</span><span class="sxs-lookup"><span data-stu-id="439e3-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="439e3-132">Ambas as entradas têm significado específico para o serviço de mensagem AB.</span><span class="sxs-lookup"><span data-stu-id="439e3-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


