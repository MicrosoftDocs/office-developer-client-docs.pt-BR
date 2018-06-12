---
title: XML para recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'O elemento de recursos no esquema XML provedor (OSC) permite que um provedor OSC especificar sua funcionalidade. Essa funcionalidade inclui o seguinte:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770953"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="ccfdc-104">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="ccfdc-104">XML for capabilities</span></span>

<span data-ttu-id="ccfdc-105">O elemento de **recursos** no esquema XML provedor (OSC) permite que um provedor OSC especificar sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="ccfdc-106">Essa funcionalidade inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ccfdc-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="ccfdc-107">Se o provedor oferece suporte à obtenção, cache ou procurando dinamicamente amigos e atividades da rede social.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="ccfdc-108">Como o OSC deve exibir certas interfaces de usuário de logon.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="ccfdc-109">Se o OSC deve usar a autenticação baseada em formulários ou configurar automaticamente os logs e redes sociais do usuário na rede social.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="ccfdc-110">O esquema XML de **recursos** é fundamental, pois ele identifica para o OSC a funcionalidade suportada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="ccfdc-111">Um provedor OSC deve implementar o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) que retorna uma cadeia de caracteres de _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="ccfdc-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="ccfdc-112">O OSC chama **ISocialProvider::GetCapabilities** para obter informações sobre os recursos do provedor do OSC na sequência de _resultado_ , o que está em conformidade com a definição de esquema XML para o elemento de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="ccfdc-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="ccfdc-113">Essas informações permitem que chamadas subsequentes provenientes do OSC para o provedor do OSC para que funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="ccfdc-114">Para especificar os recursos de um provedor OSC como um parâmetro de saída do método **ISocialProvider::GetCapabilities** , você deve estar em conformidade com o esquema XML de extensibilidade de provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="ccfdc-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="ccfdc-115">A figura a seguir mostra a estrutura do XML de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="ccfdc-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="ccfdc-116">**Figura 1. \<recursos\> estrutura XML**</span><span class="sxs-lookup"><span data-stu-id="ccfdc-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![capabilities XML structure](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="ccfdc-118">Para obter descrições detalhadas dos elementos filho do elemento de **recursos** , consulte [Elementos XML de recursos](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="ccfdc-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="ccfdc-119">Para obter um exemplo dos **recursos** de XML, consulte [Exemplo de XML de recursos](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="ccfdc-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="ccfdc-120">Para uma definição completa do esquema de XML de provedor OSC, incluindo quais elementos são obrigatórias ou opcionais, consulte [Esquema de XML para Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="ccfdc-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ccfdc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccfdc-121">See also</span></span>

- [<span data-ttu-id="ccfdc-122">Exemplo de XML de recursos</span><span class="sxs-lookup"><span data-stu-id="ccfdc-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="ccfdc-123">Sincronização de amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="ccfdc-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="ccfdc-124">XML para amigos</span><span class="sxs-lookup"><span data-stu-id="ccfdc-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="ccfdc-125">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="ccfdc-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="ccfdc-126">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="ccfdc-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

