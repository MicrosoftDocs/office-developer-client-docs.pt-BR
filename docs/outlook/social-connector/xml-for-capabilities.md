---
title: XML para recursos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'O elemento Capabilities no esquema XML do provedor (OSC) permite que um provedor do OSC especifique sua funcionalidade. Essa funcionalidade inclui o seguinte:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435002"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="c914f-104">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="c914f-104">XML for capabilities</span></span>

<span data-ttu-id="c914f-105">O elemento **Capabilities** no esquema XML do provedor (OSC) permite que um provedor do OSC especifique sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="c914f-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="c914f-106">Essa funcionalidade inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c914f-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="c914f-107">Se o provedor oferece suporte a obter, armazenar em cache ou procurar dinamicamente amigos e atividades da rede social.</span><span class="sxs-lookup"><span data-stu-id="c914f-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="c914f-108">Como o OSC deve exibir determinadas interfaces de usuário de logon.</span><span class="sxs-lookup"><span data-stu-id="c914f-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="c914f-109">Se o OSC deve usar a autenticação baseada em formulários ou configurar automaticamente a rede social e os logs no usuário na rede social.</span><span class="sxs-lookup"><span data-stu-id="c914f-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="c914f-110">O esquema XML para **recursos** é crítico porque ele identifica ao OSC a funcionalidade suportada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="c914f-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="c914f-111">Um provedor do OSC deve implementar o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) que retorna uma cadeia de caracteres de _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="c914f-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="c914f-112">O OSC chama **ISocialProvider:: GetCapabilities** para obter informações sobre os recursos do provedor OSC na cadeia de caracteres de _resultado_ , que está em conformidade com a definição de esquema XML para o elemento **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c914f-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="c914f-113">Essas informações permitem que chamadas subsequentes do OSC para o provedor do OSC funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="c914f-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="c914f-114">Para especificar recursos de um provedor do OSC como um parâmetro de saída do método **ISocialProvider:: GetCapabilities** , você deve estar em conformidade com o esquema XML de extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="c914f-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="c914f-115">A figura a seguir mostra a estrutura XML dos **recursos** .</span><span class="sxs-lookup"><span data-stu-id="c914f-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="c914f-116">**Figura 1. \<estrutura\> XML de recursos**</span><span class="sxs-lookup"><span data-stu-id="c914f-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![capabilities XML structure](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="c914f-118">Para obter descrições detalhadas dos elementos filho do elemento **Capabilities** , consulte [Capabilities elementos XML](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="c914f-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="c914f-119">Para obter um exemplo do XML de **recursos**, consulte [Exemplo do XML de recursos](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="c914f-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="c914f-120">Para obter uma definição completa do esquema XML do provedor OSC, incluindo quais elementos são obrigatórios ou opcionais, consulte [esquema XML do provedor do Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c914f-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c914f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c914f-121">See also</span></span>

- [<span data-ttu-id="c914f-122">Exemplo do XML de recursos</span><span class="sxs-lookup"><span data-stu-id="c914f-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="c914f-123">Sincronizar amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="c914f-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="c914f-124">XML para amigos</span><span class="sxs-lookup"><span data-stu-id="c914f-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="c914f-125">XML para atividades</span><span class="sxs-lookup"><span data-stu-id="c914f-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="c914f-126">Desenvolvimento de um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="c914f-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

