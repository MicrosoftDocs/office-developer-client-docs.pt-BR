---
title: Desenvolvimento com o Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Você pode aprimorar a funcionalidade de formulários do InfoPath estendendo-as com código gerenciado desenvolvido no Visual Studio 2012. Em seguida, você pode publicar os formulários com o código para bibliotecas de formulários no SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300284"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="37189-104">Desenvolvimento com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37189-104">Develop with Visual Studio</span></span>

<span data-ttu-id="37189-105">Você pode aprimorar a funcionalidade de formulários do InfoPath estendendo-as com código gerenciado desenvolvido no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="37189-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="37189-106">Em seguida, você pode publicar os formulários com o código para bibliotecas de formulários no SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37189-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="37189-107">Você pode iniciar a programação e implantar os formulários do InfoPath com código gerenciado em três etapas de alto nível:</span><span class="sxs-lookup"><span data-stu-id="37189-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="37189-108">Instalar o Visual Studio 2012 com o complemento[Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807).</span><span class="sxs-lookup"><span data-stu-id="37189-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="37189-109">Definir o idioma de programação, escrever e depurar código no editor de código do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="37189-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="37189-110">Quando terminar de criar o formulário e desenvolver o código, o modelo de formulário poderá ser publicado para o SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="37189-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="37189-111">Aqui estão alguns motivos para considerar a criação de formulários que são compatíveis com o SharePoint Server 2013:</span><span class="sxs-lookup"><span data-stu-id="37189-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="37189-112">Formulários do SharePoint Server 2013 com o InfoPath Forms Services implantados podem ser preenchidos em um navegador.</span><span class="sxs-lookup"><span data-stu-id="37189-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="37189-113">Isso permite aos usuários que não tenham o InfoPath instalado abrir e usar formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="37189-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="37189-114">Criar apenas uma versão do formulário.</span><span class="sxs-lookup"><span data-stu-id="37189-114">You design only one version of the form.</span></span> <span data-ttu-id="37189-115">Formulários que são compatíveis com o Microsoft SharePoint Server também são compatíveis com o InfoPath Filler, mas os formulários que são compatíveis somente com o InfoPath Filler não podem ser abertos no navegador.</span><span class="sxs-lookup"><span data-stu-id="37189-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="37189-116">Há duas maneiras para publicar seu formulário no SharePoint: solução de área restrita e implantação do administrador do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="37189-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="37189-117">Confira mais informações sobre cada método de publicação para obter sugestões sobre qual método é o mais adequado para seu cenário.Veja [formulários de publicação com o código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="37189-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="37189-118">Para exemplos de soluções de área restrita, consulte [soluções de área restrita exemplo](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="37189-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="37189-119">Desenvolvendo com o Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37189-119">Developing with Visual Studio</span></span>

<span data-ttu-id="37189-120">Com o Visual Studio 2012 e no Microsoft Visual Studio Tools for Applications 2012 aplicativos instalados, você está pronto para iniciar a desenvolver soluções de código de gerenciamento do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="37189-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="37189-121">Escolher uma linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="37189-121">Choosing a Programming Language</span></span>

<span data-ttu-id="37189-122">InfoPath fornece opções para o programa em quatro versões do modelo de objeto do InfoPath em dois idiomas: Visual Basic e c#.</span><span class="sxs-lookup"><span data-stu-id="37189-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="37189-123">As quatro versões do modelo de objeto proporcionam uma compatibilidade com o InfoPath 2013, o InfoPath, o Office InfoPath 2007 e o Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="37189-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="37189-124">Para especificar o modelo de programação de idioma e objetos</span><span class="sxs-lookup"><span data-stu-id="37189-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="37189-125">Com um projeto de modelo de formulário aberto no InfoPath designer, clique em **idioma** no **guia** do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="37189-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="37189-126">Na categoria **programação** das **opções de formulário** na caixa de diálogo, selecione o idioma que deseja para trabalhar com**a lista suspensa** no código de linguagem do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="37189-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="37189-127">Em seguida, selecione a versão do modelo de objeto da **versão de destino** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="37189-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="37189-128">A opção **versão de destino** compatível com o InfoPath 2013 não tem a versão do ano seguinte no**nome** Infopath.</span><span class="sxs-lookup"><span data-stu-id="37189-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="37189-129">Nem todos os tipos de modelo de formulário suportam código.</span><span class="sxs-lookup"><span data-stu-id="37189-129">Not all form template types support code.</span></span> <span data-ttu-id="37189-130">Por exemplo, na **lista do SharePoint** o tipo de modelo de formulário e as **partes de modelo** não suportam código do formulário.</span><span class="sxs-lookup"><span data-stu-id="37189-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="37189-131">Ao criar um tipo de modelo de formulário que não suporte código, o guia**desenvolvedor** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="37189-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="37189-132">Além disso, alguns tipos de modelos formulário suportam todas as quatro versões do modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="37189-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="37189-133">Por exemplo, o modelo**formulário em branco (InfoPath Filler)** oferece suporte a todas as quatro versões do modelo de objeto (e cria um modelo de formulário compatíveis com o InfoPath Filler nessas versões), mas o **Formulário** modelo em branco suporta apenas o InfoPath 2013 e o InfoPath (e cria modelos de formulário compatíveis com o InfoPath Filler e navegador).</span><span class="sxs-lookup"><span data-stu-id="37189-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="37189-134">Você pode definir um padrão de linguagem de programação para que o designer de formulário do InfoPath sempre comece com a versão de idioma e o objeto de modelo de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="37189-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="37189-135">Para definir o padrão de linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="37189-135">To set the default programming language</span></span>

1. <span data-ttu-id="37189-136">Clique na guia **Arquivo** e, em seguida, em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="37189-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="37189-137">Na **seção** geral\*\* da caixa de diálogo\*\* do InfoPath, clique em **mais opções**.</span><span class="sxs-lookup"><span data-stu-id="37189-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="37189-138">No guia **Design \*\* nas **opções** da caixa de diálogo, escolha a programação de idioma padrão na seção**programação padrões\*\*.</span><span class="sxs-lookup"><span data-stu-id="37189-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="37189-139">Escrever códigos</span><span class="sxs-lookup"><span data-stu-id="37189-139">Writing Code</span></span>

<span data-ttu-id="37189-140">Agora você pode começar desenvolver com o InfoPath 2013 e o Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="37189-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="37189-141">Para iniciar o Editor do Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="37189-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="37189-142">Abra um modelo de formulário no InfoPath designer.</span><span class="sxs-lookup"><span data-stu-id="37189-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="37189-143">Clique em **Editor de código** no **guia** desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="37189-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="37189-144">Você também pode iniciar o editor de código e adicionar automaticamente manipuladores de eventos para eventos de formulário e controle usando comandos na guia**desenvolvedor** menus de contexto e outros métodos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="37189-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="37189-145">Para saber mais, confira [adicionar um manipulador de eventos](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="37189-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

