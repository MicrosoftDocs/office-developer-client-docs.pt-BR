---
title: Escolher um conjunto de propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5680fed2-b2e7-4c4b-9ba8-2c497b9c433c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d983b71c7c92c395740a8ae6f6d3666a8bc2c0c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407190"
---
# <a name="choosing-a-forms-property-set"></a><span data-ttu-id="94f46-103">Escolher um conjunto de propriedades do formulário</span><span class="sxs-lookup"><span data-stu-id="94f46-103">Choosing a form's property set</span></span>

<span data-ttu-id="94f46-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94f46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94f46-105">Ao implementar seu servidor de formulários, você precisa ter uma propriedade para cada informação de que sua classe de mensagens precisa.</span><span class="sxs-lookup"><span data-stu-id="94f46-105">When you implement your form server, you need to have a property for each piece of information that your message class needs.</span></span> <span data-ttu-id="94f46-106">Essas propriedades podem ser propriedades MAPI predefinidas ou podem ser Propriedades personalizadas definidas por você.</span><span class="sxs-lookup"><span data-stu-id="94f46-106">These properties can be predefined MAPI properties, or they can be custom properties that you define.</span></span> <span data-ttu-id="94f46-107">Para obter mais informações sobre como trabalhar com propriedades, consulte [MAPI Property Overview](mapi-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94f46-107">For more information about working with properties, see [MAPI Property Overview](mapi-property-overview.md).</span></span>
  
<span data-ttu-id="94f46-108">Seu arquivo de configuração de formulário conterá uma lista de propriedades que seu servidor de formulário expõe para que os aplicativos cliente usem, mas isso não precisa ser a lista completa de propriedades usadas pelo seu servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="94f46-108">Your form configuration file will contain a list of properties that your form server exposes for client applications to use, but this does not have to be the entire list of properties used by your form server.</span></span> <span data-ttu-id="94f46-109">Os aplicativos clientes normalmente usam as propriedades expostas para permitir que os usuários classifiquem mensagens em uma pasta ou personalizem suas interfaces de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="94f46-109">Client applications typically use the exposed properties to enable users to sort messages in a folder or customize their interfaces in some way.</span></span>
  
<span data-ttu-id="94f46-110">O MAPI tem um amplo conjunto de propriedades predefinidas que são suficientes para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="94f46-110">MAPI has a large set of predefined properties that suffice for most applications.</span></span> <span data-ttu-id="94f46-111">No enTanto, haverá ocasiões em que uma classe de mensagem personalizada precisa de uma propriedade que MAPI não define.</span><span class="sxs-lookup"><span data-stu-id="94f46-111">However, there will be times when a custom message class needs a property that MAPI does not define.</span></span> <span data-ttu-id="94f46-112">Você pode usar propriedades personalizadas para estender o conjunto de propriedades predefinido MAPI para qualquer informação especial que seu servidor de formulário precisa suportar.</span><span class="sxs-lookup"><span data-stu-id="94f46-112">You can use custom properties to extend the MAPI predefined set of properties for whatever special information your form server needs to support.</span></span>
  
<span data-ttu-id="94f46-113">Você pode usar uma das seguintes maneiras para definir propriedades personalizadas:</span><span class="sxs-lookup"><span data-stu-id="94f46-113">You can use either of the following ways to define custom properties:</span></span>
  
- <span data-ttu-id="94f46-114">Escolha um nome para a propriedade e use o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter uma marca de propriedade para ela.</span><span class="sxs-lookup"><span data-stu-id="94f46-114">Choose a name for the property and use the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method to obtain a property tag for it.</span></span> <span data-ttu-id="94f46-115">A interface [IMAPIProp](imapipropiunknown.md) através da qual você chama esse método vem do ponteiro [IMessage](imessageimapiprop.md) que é passado para o servidor de formulário quando a mensagem é criada.</span><span class="sxs-lookup"><span data-stu-id="94f46-115">The [IMAPIProp](imapipropiunknown.md) interface through which you call this method comes from the [IMessage](imessageimapiprop.md) pointer that is passed to the form server when the message is created.</span></span> <span data-ttu-id="94f46-116">Observe que o nome da propriedade deve ser uma cadeia de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="94f46-116">Note that the property name must be a wide-character string.</span></span> 
    
- <span data-ttu-id="94f46-117">Defina você mesmo uma marca de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="94f46-117">Define a custom property tag yourself.</span></span> <span data-ttu-id="94f46-118">As marcas de propriedade personalizada devem estar no intervalo 0x6800 a 0x7BFF.</span><span class="sxs-lookup"><span data-stu-id="94f46-118">Custom property tags must be in the range 0x6800 through 0x7BFF.</span></span> <span data-ttu-id="94f46-119">As propriedades desse intervalo são específicas de classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="94f46-119">Properties in this range are message-class specific.</span></span>
    
<span data-ttu-id="94f46-120">Para obter mais informações sobre como definir propriedades personalizadas, consulte [definindo novas propriedades MAPI](defining-new-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="94f46-120">For more information about defining custom properties, see [Defining New MAPI Properties](defining-new-mapi-properties.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="94f46-121">Os servidores de formulário que possuem um texto de mensagem geralmente usam a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) para armazená-lo.</span><span class="sxs-lookup"><span data-stu-id="94f46-121">Form servers that have a message text often use the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to store it.</span></span> <span data-ttu-id="94f46-122">Se o seu servidor de formulário usa o **PR_RTF_COMPRESSED**, ele também deve garantir que a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) contenha uma versão somente texto do texto da mensagem, caso a mensagem resultante seja lida por um cliente que não ofereça suporte a Rich Text Texto da mensagem de formato (RTF).</span><span class="sxs-lookup"><span data-stu-id="94f46-122">If your form server uses **PR_RTF_COMPRESSED**, it should also ensure that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property contains a text-only version of the message text, in case the resulting message is read by a client that does not support Rich Text Format (RTF) message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94f46-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="94f46-123">See also</span></span>

- [<span data-ttu-id="94f46-124">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="94f46-124">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

