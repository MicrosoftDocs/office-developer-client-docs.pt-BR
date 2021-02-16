---
title: Aplicando um modelo de provedor de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Os modelos de provedor do Outlook Social Connector (OSC) de exemplo lhe dão uma estrutura para implementar um provedor do OSC. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425908"
---
# <a name="applying-a-sample-provider-template"></a><span data-ttu-id="a2310-103">Aplicando um modelo de provedor de exemplo</span><span class="sxs-lookup"><span data-stu-id="a2310-103">Applying a Sample Provider Template</span></span>

<span data-ttu-id="a2310-104">Os modelos de provedor do Outlook Social Connector (OSC) de exemplo lhe dão uma estrutura para implementar um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="a2310-104">The sample Outlook Social Connector (OSC) provider templates give you a framework for implementing an OSC provider.</span></span> <span data-ttu-id="a2310-105">Os modelos de provedor estão disponíveis em C++, C# e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2310-105">The provider templates are available in C++, C#, and Visual Basic.</span></span> <span data-ttu-id="a2310-106">Esses modelos são apenas um ponto de partida para o desenvolvimento do provedor; os modelos não abordam a escrita do código de implementação para o provedor e a criação de um pacote de instalação para o provedor.</span><span class="sxs-lookup"><span data-stu-id="a2310-106">These templates are just a starting point for your provider development; the templates do not address writing the implementation code for the provider and creating a setup package for the provider.</span></span> <span data-ttu-id="a2310-107">O procedimento a seguir mostra como aplicar um modelo de provedor osC quando você começa a desenvolver um provedor.</span><span class="sxs-lookup"><span data-stu-id="a2310-107">The following procedure shows how to apply an OSC provider template when you begin to develop a provider.</span></span>
  
### <a name="to-apply-an-osc-provider-template"></a><span data-ttu-id="a2310-108">Para aplicar um modelo de provedor osC</span><span class="sxs-lookup"><span data-stu-id="a2310-108">To apply an OSC provider template</span></span>

1. <span data-ttu-id="a2310-109">No menu **Iniciar,** clique com o botão direito do mouse **no Microsoft Visual Studio 2010** e clique no comando Executar **como** administrador.</span><span class="sxs-lookup"><span data-stu-id="a2310-109">On the **Start** menu, right-click **Microsoft Visual Studio 2010** and click the **Run as administrator** command.</span></span> <span data-ttu-id="a2310-110">Quando solicitado, clique em **Sim para** executar o Visual Studio como administrador.</span><span class="sxs-lookup"><span data-stu-id="a2310-110">When prompted, click **Yes** to run Visual Studio as an administrator.</span></span> 
    
2. <span data-ttu-id="a2310-111">Altere o nome do projeto e o namespace no modelo para os identificadores de namespace e nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="a2310-111">Change the project name and namespace in the template to your project name and namespace identifiers.</span></span>
    
3. <span data-ttu-id="a2310-112">Modifique **a classe AssemblyInfo** para especificar as informações de assembly apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a2310-112">Modify the **AssemblyInfo** class to specify the appropriate assembly information.</span></span> 
    
4. <span data-ttu-id="a2310-113">Implemente os membros da interface marcados **como To-Do** e adicione mais dependências e referências, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="a2310-113">Implement the interface members marked as **To-Do** and add more dependencies and references, as required.</span></span> 
    
5. <span data-ttu-id="a2310-114">Compile o projeto.</span><span class="sxs-lookup"><span data-stu-id="a2310-114">Build the project.</span></span>
    
6. <span data-ttu-id="a2310-115">Verifique se o ProgID do assembly do provedor está listado como uma chave em  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .</span><span class="sxs-lookup"><span data-stu-id="a2310-115">Ensure that the provider assembly ProgID is listed as a key under  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
7. <span data-ttu-id="a2310-116">Para distribuir o projeto de instalação, crie um projeto de instalação no Visual Studio ou uma ferramenta de instalação de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="a2310-116">To distribute the setup project, create a setup project in Visual Studio or a setup tool of your choice.</span></span>
    
8. <span data-ttu-id="a2310-117">Seu projeto de instalação deve concluir o registro COM para seu assembly e também criar a chave ProgID conforme listado na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="a2310-117">Your setup project should complete COM registration for your assembly and also create the ProgID key as listed in step 5.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2310-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2310-118">See also</span></span>

- [<span data-ttu-id="a2310-119">Baixando os exemplos</span><span class="sxs-lookup"><span data-stu-id="a2310-119">Downloading the Samples</span></span>](downloading-the-samples.md)
- [<span data-ttu-id="a2310-120">Modelos de exemplo do OSC</span><span class="sxs-lookup"><span data-stu-id="a2310-120">OSC Sample Templates</span></span>](osc-sample-templates.md)

