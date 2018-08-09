---
title: Entradas de propriedades nas seções do serviço de mensagens MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30f5e0b59bacfab91a3a6c77c0b345d6299df9e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770180"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="63b24-103">Entradas de propriedades nas seções do serviço de mensagens MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="63b24-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="63b24-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63b24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63b24-105">Entradas de definir propriedades usam o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="63b24-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="63b24-106">**marca de propriedade** **=** o valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="63b24-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="63b24-107">A marca de propriedade pode ser uma marca de propriedade MAPI padrão se os dados de configuração representam uma das propriedades predefinidas pelo MAPI ou uma marca de não-padrão se os dados não representam uma propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="63b24-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="63b24-108">A marca de não-padrão é feita, combinando o valor de um identificador de propriedade com um tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="63b24-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="63b24-109">O resultado é um número hexadecimal de 8 dígitos.</span><span class="sxs-lookup"><span data-stu-id="63b24-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="63b24-110">O valor da propriedade pode ser qualquer item faz sentido para a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="63b24-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="63b24-111">Seções do serviço de mensagem podem conter várias entradas, dependendo do serviço de mensagem que está sendo configurado.</span><span class="sxs-lookup"><span data-stu-id="63b24-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="63b24-112">Normalmente, as seguintes propriedades MAPI são incluídas em uma seção de serviços de mensagem no formato listado:</span><span class="sxs-lookup"><span data-stu-id="63b24-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="63b24-113">**PR_DISPLAY_NAME** =  _cadeia de caracteres_</span><span class="sxs-lookup"><span data-stu-id="63b24-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="63b24-114">**PR_SERVICE_DLL_NAME** =  _nome do arquivo DLL_</span><span class="sxs-lookup"><span data-stu-id="63b24-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="63b24-115">**PR_SERVICE_ENTRY_NAME** =  _nome da função de ponto de entrada_</span><span class="sxs-lookup"><span data-stu-id="63b24-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="63b24-116">**PR_SERVICE_SUPPORT_FILES** =  _lista de arquivos_</span><span class="sxs-lookup"><span data-stu-id="63b24-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="63b24-117">**PR_SERVICE_DELETE_FILES** =  _lista de arquivos_</span><span class="sxs-lookup"><span data-stu-id="63b24-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="63b24-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span><span class="sxs-lookup"><span data-stu-id="63b24-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="63b24-119">A cadeia de caracteres **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) é o nome do serviço na mensagem que é mostrado na interface do usuário, o nome que o usuário associa o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b24-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="63b24-120">O nome de exibição é uma entrada opcional em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="63b24-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="63b24-121">Em alguns casos, o nome para exibição será composto de duas partes; uma parte atribuído pelo serviço de mensagem e uma parte atribuído pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="63b24-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="63b24-122">Se o usuário é responsável pela atribuição de uma das partes, isso normalmente é tratado com uma caixa de diálogo especial conhecida como uma folha de propriedades fornecida pelo serviço de mensagem sob o controle de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="63b24-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="63b24-123">As informações fornecidas para a entrada de **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) são o nome da DLL que contém o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b24-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="63b24-124">As informações fornecidas para a entrada de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) são o nome da função de ponto de entrada dentro desse DLL que chamadas MAPI para configurar o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b24-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="63b24-125">Os arquivos listados na entrada **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) são arquivos que devem ser instalados com o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b24-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="63b24-126">Da mesma forma, os arquivos na entrada **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) devem ser removidos quando o serviço de mensagem é removido.</span><span class="sxs-lookup"><span data-stu-id="63b24-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="63b24-127">A entrada **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) é uma coleção das opções definidas para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63b24-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="63b24-128">Por exemplo, o bit SERVICE_SINGLE_COPY é definido quando o serviço de mensagem pode aparecer apenas uma vez em um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="63b24-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="63b24-129">SERVICE_NO_PRIMARY_IDENTITY estará definido o bit é definido se o serviço de mensagem não fornece informações de identidade.</span><span class="sxs-lookup"><span data-stu-id="63b24-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="63b24-130">Siga a dois exemplos de entradas de propriedade não-padrão.</span><span class="sxs-lookup"><span data-stu-id="63b24-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="63b24-131">A primeira entrada especifica o caminho para o arquivo usado pelo catálogo de endereços padrão como o valor da propriedade; a segunda entrada especifica um valor de propriedade numéricos.</span><span class="sxs-lookup"><span data-stu-id="63b24-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="63b24-132">As duas entradas têm significado específico ao serviço de mensagens de AB.</span><span class="sxs-lookup"><span data-stu-id="63b24-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


