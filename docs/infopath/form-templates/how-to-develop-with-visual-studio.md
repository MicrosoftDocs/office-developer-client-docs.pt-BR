---
title: Desenvolver com o Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Você pode aprimorar a funcionalidade dos formulários do InfoPath bastante estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar seus formulários com código bibliotecas de formulários no SharePoint Server 2013.
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765625"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="f1322-104">Desenvolver com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1322-104">Develop with Visual Studio</span></span>

<span data-ttu-id="f1322-105">Você pode aprimorar a funcionalidade dos formulários do InfoPath bastante estendendo-as com código gerenciado desenvolvido no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f1322-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="f1322-106">Em seguida, você pode publicar seus formulários com código bibliotecas de formulários no SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1322-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="f1322-107">Você pode iniciar a programação e a implantação de formulários do InfoPath com código gerenciado em três etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="f1322-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="f1322-108">Instale o Visual Studio 2012 com o complemento do [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) .</span><span class="sxs-lookup"><span data-stu-id="f1322-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="f1322-109">Definir sua linguagem de programação e, em seguida, escrever e depurar código no editor de código do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f1322-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="f1322-110">Quando você concluir a criação do formulário e desenvolvimento de seu código, o modelo de formulário pode ser publicado para o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f1322-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="f1322-111">Aqui estão algumas razões para considerar a criação de formulários que são compatíveis com o SharePoint Server 2013:</span><span class="sxs-lookup"><span data-stu-id="f1322-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="f1322-112">Formulários implantados para o SharePoint Server 2013 com o InfoPath Forms Services podem ser preenchidos em um navegador.</span><span class="sxs-lookup"><span data-stu-id="f1322-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="f1322-113">Isso permite que os usuários que não têm instalado para abrir e usar os formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f1322-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="f1322-114">Projetar apenas uma versão do formulário.</span><span class="sxs-lookup"><span data-stu-id="f1322-114">You design only one version of the form.</span></span> <span data-ttu-id="f1322-115">Formulários que são compatíveis com o Microsoft SharePoint Server também são compatíveis com o InfoPath Filler, mas os formulários que são compatíveis apenas com o InfoPath Filler não podem ser abertos no navegador.</span><span class="sxs-lookup"><span data-stu-id="f1322-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="f1322-116">Existem duas maneiras de publicar o formulário para o SharePoint: SharePoint soluções em área restrita e soluções implantados pelo administrador.</span><span class="sxs-lookup"><span data-stu-id="f1322-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="f1322-117">Para obter mais informações sobre cada método de publicação e sugestões sobre qual método é melhor para seu cenário, consulte [Publicando formulários com código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="f1322-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="f1322-118">Por exemplo, soluções para soluções em área restrita, consulte [Exemplos de soluções em área restrita](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="f1322-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="f1322-119">Desenvolvendo com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1322-119">Developing with Visual Studio</span></span>

<span data-ttu-id="f1322-120">Com o Visual Studio 2012 e o Microsoft Visual Studio Tools para o complemento aplicativos 2012 instalado, você estará pronto para começar a desenvolver soluções de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f1322-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="f1322-121">Escolher um idioma de programação</span><span class="sxs-lookup"><span data-stu-id="f1322-121">Choosing a Programming Language</span></span>

<span data-ttu-id="f1322-122">InfoPath fornece as opções para programar usando quatro versões do modelo de objeto do InfoPath em dois idiomas: Visual Basic e c#.</span><span class="sxs-lookup"><span data-stu-id="f1322-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="f1322-123">As quatro versões do modelo de objeto fornecem compatibilidade com o InfoPath 2013, InfoPath, Office InfoPath 2007 e Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="f1322-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="f1322-124">Para especificar o modelo de objeto e da linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="f1322-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="f1322-125">Com um projeto de modelo de formulário aberto no InfoPath designer, clique em **idioma** , na guia **desenvolvedor** .</span><span class="sxs-lookup"><span data-stu-id="f1322-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="f1322-126">Na categoria **programação** da caixa de diálogo **Opções de formulário** , selecione o idioma que você deseja trabalhar com na lista suspensa **linguagem de código do modelo de formulário** .</span><span class="sxs-lookup"><span data-stu-id="f1322-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="f1322-127">Em seguida, selecione a versão do modelo de objeto da lista suspensa de **versão de destino** .</span><span class="sxs-lookup"><span data-stu-id="f1322-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="f1322-128">A opção de **versão de destino** é compatível com o InfoPath 2013 não tem um versão ano depois do nome do **InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="f1322-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f1322-129">Nem todos os tipos de modelo de formulário suportam de código.</span><span class="sxs-lookup"><span data-stu-id="f1322-129">Not all form template types support code.</span></span> <span data-ttu-id="f1322-130">Por exemplo, o tipo de modelo de formulário de **Lista do SharePoint** e **Partes do modelo** não suportam o código de formulário.</span><span class="sxs-lookup"><span data-stu-id="f1322-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="f1322-131">Ao criar um tipo de modelo de formulário que não oferece suporte a código, a guia **desenvolvedor** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="f1322-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="f1322-132">Além disso, somente alguns tipos de modelo de formulário suportam a todas as quatro versões do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="f1322-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="f1322-133">Por exemplo, o tipo de modelo de **Formulário em branco (InfoPath Filler)** oferece suporte a todas as quatro versões do modelo de objeto (e cria um modelo de formulário que são compatíveis apenas com o InfoPath Filler nessas versões), mas o modelo de **Formulário em branco** suporta apenas InfoPath 2013 e InfoPath (e cria os modelos de formulário compatíveis com o InfoPath Filler e o navegador).</span><span class="sxs-lookup"><span data-stu-id="f1322-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="f1322-134">Você pode definir um padrão de linguagem de programação para que o designer de formulários do InfoPath sempre iniciará com a versão de modelo de objeto e de idioma de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="f1322-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="f1322-135">Para definir o padrão de linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="f1322-135">To set the default programming language</span></span>

1. <span data-ttu-id="f1322-136">Clique na guia **arquivo** e, em seguida, clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="f1322-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="f1322-137">Na seção **Geral** da caixa de diálogo **Opções do InfoPath** , clique em **Mais opções**.</span><span class="sxs-lookup"><span data-stu-id="f1322-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="f1322-138">Na guia **Design** da caixa de diálogo **Opções** , selecione a linguagem na seção **Padrões de programação** de programação padrão.</span><span class="sxs-lookup"><span data-stu-id="f1322-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="f1322-139">Escrevendo códigos</span><span class="sxs-lookup"><span data-stu-id="f1322-139">Writing Code</span></span>

<span data-ttu-id="f1322-140">Agora, você pode começar a desenvolver com InfoPath 2013 e o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f1322-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="f1322-141">Para iniciar o Editor de código do Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1322-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="f1322-142">Abra um modelo de formulário no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f1322-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="f1322-143">Na guia **desenvolvedor** , clique em **Editor de código** .</span><span class="sxs-lookup"><span data-stu-id="f1322-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="f1322-144">Também pode iniciar o editor de código e adicionar automaticamente os manipuladores de eventos para o formulário e controlar eventos usando os comandos na guia **desenvolvedor** , menus de contexto e outros métodos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f1322-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="f1322-145">Para obter mais informações, consulte [Adicionar um manipulador de eventos](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="f1322-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

