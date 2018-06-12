---
title: Escolhendo o conjunto de propriedades de um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 456ef036b26fd8b9840d33f0f699474c3a6ce127
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766288"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="8635b-103">Escolhendo o conjunto de propriedades de um formulário</span><span class="sxs-lookup"><span data-stu-id="8635b-103">Choosing a form's property set</span></span>

<span data-ttu-id="8635b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8635b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8635b-105">Quando você implementa o seu servidor de formulário, você precisa ter uma propriedade para cada parte da informação que precisa de sua classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8635b-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="8635b-106">Essas propriedades podem ser propriedades predefinidas de MAPI ou eles podem ser propriedades personalizadas que você define.</span><span class="sxs-lookup"><span data-stu-id="8635b-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="8635b-107">Para obter mais informações sobre como trabalhar com propriedades, consulte [Visão geral de propriedade de MAPI](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8635b-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="8635b-108">Seu arquivo de configuração do formulário irá conter uma lista de propriedades que seu servidor de formulário expõe para aplicativos de cliente usar, mas isso não precisa ser a lista completa de propriedades usadas pelo seu servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="8635b-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="8635b-109">Aplicativos cliente geralmente usam as propriedades expostas para habilitar usuários ordenar as mensagens em uma pasta ou personalizar suas interfaces de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="8635b-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="8635b-110">MAPI tem um grande conjunto de propriedades predefinidas que suficiente para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8635b-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="8635b-111">No entanto, haverá vezes quando uma classe de mensagem personalizado precisa de uma propriedade de MAPI não define.</span><span class="sxs-lookup"><span data-stu-id="8635b-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="8635b-112">Você pode usar as propriedades personalizadas para estender o conjunto MAPI predefinido de propriedades para qualquer informações especiais que seu servidor de formulário precisa suportar.</span><span class="sxs-lookup"><span data-stu-id="8635b-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="8635b-113">Você pode usar qualquer uma das seguintes maneiras para definir propriedades personalizadas:</span><span class="sxs-lookup"><span data-stu-id="8635b-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="8635b-114">Escolha um nome para a propriedade e use o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter uma marca de propriedade para ele.</span><span class="sxs-lookup"><span data-stu-id="8635b-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="8635b-115">A interface [IMAPIProp](imapipropiunknown.md) através do qual você chamar este método proveniente o ponteiro [IMessage](imessageimapiprop.md) que é passado para o servidor de formulário quando a mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="8635b-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="8635b-116">Observe que o nome da propriedade deve ser uma cadeia de caracteres a toda a.</span><span class="sxs-lookup"><span data-stu-id="8635b-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="8635b-117">Defina uma marca de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="8635b-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="8635b-118">Marcas de propriedade personalizada devem estar no intervalo 0x6800 por meio de 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="8635b-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="8635b-119">As propriedades deste intervalo são classe de mensagem específicos.</span><span class="sxs-lookup"><span data-stu-id="8635b-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="8635b-120">Para obter mais informações sobre como definir propriedades personalizadas, consulte [Definindo novas propriedades de MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8635b-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="8635b-121">Servidores de formulário que têm um texto de mensagem com frequência usam a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para armazená-lo.</span><span class="sxs-lookup"><span data-stu-id="8635b-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="8635b-122">Se o seu servidor de formulário usa **PR_RTF_COMPRESSED**, ele também deve assegurar que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contém uma versão somente texto do texto da mensagem, caso a mensagem resultante é lido por um cliente que não oferece suporte a Rich Text Texto da mensagem Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="8635b-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8635b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8635b-123">See also</span></span>

- [<span data-ttu-id="8635b-124">Desenvolvimento de servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="8635b-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

