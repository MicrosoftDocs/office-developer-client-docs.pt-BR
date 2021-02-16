---
title: Visualizar e depurar modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- visualização de modelos de formulário [infopath 2007], modelos de formulário de depuração [InfoPath 2007], modelos de formulário [InfoPath 2007], visualização,depuração [InfoPath 2007], modelos de formulário de código gerenciado, modelos de formulário [InfoPath 2007], depuração,InfoPath 2007, modelos de formulário de depuração,InfoPath 2007, visualização de modelos de formulário
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: O Microsoft InfoPath com Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, seu projeto é compilado e o InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele é encontrada, o foco se move para o editor de código. Quando você continua após um ponto de interrupção, o foco volta para a janela de visualização. A depuração para quando você fecha a janela de visualização.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405237"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="e5126-108">Visualizar e depurar modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="e5126-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="e5126-109">O Microsoft InfoPath com Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="e5126-109">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode.</span></span> <span data-ttu-id="e5126-110">Quando você inicia a depuração de código de formulário, seu projeto é compilado e o InfoPath exibe seu formulário na janela de visualização do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e5126-110">When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window.</span></span> <span data-ttu-id="e5126-111">Quando uma linha de código que tem um ponto de interrupção definido para ele é encontrada, o foco se move para o editor de código.</span><span class="sxs-lookup"><span data-stu-id="e5126-111">When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor.</span></span> <span data-ttu-id="e5126-112">Quando você continua após um ponto de interrupção, o foco volta para a janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="e5126-112">When you continue past a breakpoint, the focus moves back to the preview window.</span></span> <span data-ttu-id="e5126-113">A depuração para quando você fecha a janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="e5126-113">Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="e5126-114">Você também pode modificar as opções de formulário do modelo de formulário para visualizar e depurar usando uma função de usuário específica, um arquivo de dados de exemplo ou especificando o domínio no qual o formulário será publicado.</span><span class="sxs-lookup"><span data-stu-id="e5126-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e5126-115">Não é possível depurar modelos de formulário depois que eles são implantados em tempo de executar do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="e5126-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="e5126-116">Isso inclui modelos de formulário que são compatíveis apenas com o InfoPath, bem como aqueles compatíveis com o InfoPath e o navegador da Web usando o InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="e5126-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="e5126-117">No entanto, é possível registrar valores em um campo do código em tempo de executar para ajudar na depuração da lógica de negócios de um modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="e5126-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="e5126-118">Para obter informações sobre como fazer isso, consulte [Valores de log para um campo para depuração.](how-to-log-values-to-a-field-for-debugging.md)</span><span class="sxs-lookup"><span data-stu-id="e5126-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="e5126-119">Depuração no modo de visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="e5126-120">Para depurar um projeto do InfoPath no Modo de Visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="e5126-121">Criar ou abrir um modelo de formulário de código gerenciado do InfoPath no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="e5126-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="e5126-122">De definir um ou mais pontos de interrupção em seu código de formulário no editor de código clicando na barra cinza à esquerda da linha de código onde você deseja inserir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="e5126-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="e5126-123">Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="e5126-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="e5126-124">No menu **Depurar,** clique **em Iniciar Depuração**; ou pressione F5.</span><span class="sxs-lookup"><span data-stu-id="e5126-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="e5126-125">O projeto será compilado e o formulário será exibido na janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="e5126-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="e5126-126">Interagir com o formulário até que uma linha de código contendo um ponto de interrupção seja encontrada.</span><span class="sxs-lookup"><span data-stu-id="e5126-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="e5126-127">O foco retorna ao editor de código.</span><span class="sxs-lookup"><span data-stu-id="e5126-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="e5126-128">No menu **Depurar,** clique em **Continuar**; ou pressione F5.</span><span class="sxs-lookup"><span data-stu-id="e5126-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="e5126-129">Quando terminar a depuração, feche a janela de visualização; ou no menu **Depurar,** clique em **Parar Depuração.**</span><span class="sxs-lookup"><span data-stu-id="e5126-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e5126-130">Para depurar um modelo de formulário de código gerenciado do InfoPath ao usar um membro do modelo de objeto que exija confiança total, você deve configurar seu modelo de formulário conforme descrito em Visualizar e Depurar Modelos de Formulário que Exigem Confiança [Total.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)</span><span class="sxs-lookup"><span data-stu-id="e5126-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="e5126-131">Usando um arquivo de dados de exemplo</span><span class="sxs-lookup"><span data-stu-id="e5126-131">Using a Sample Data File</span></span>

<span data-ttu-id="e5126-132">Por padrão, a depuração e a visualização usam template.xml arquivo criado quando um modelo de formulário é criado.</span><span class="sxs-lookup"><span data-stu-id="e5126-132">By default, debugging and previewing uses the template.xml file that is created when a form template is created.</span></span> <span data-ttu-id="e5126-133">Você pode criar seu próprio arquivo de dados e especificar usá-lo ao visualizar ou depurar usando um dos procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5126-133">You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="e5126-134">Para especificar um arquivo de dados de exemplo a ser usado durante a depuração ou visualização no Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="e5126-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="e5126-135">Para exibir template.xml, abra o modelo de formulário no modo de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e5126-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="e5126-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click Source **Files**.</span><span class="sxs-lookup"><span data-stu-id="e5126-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="e5126-137">Salve os arquivos de modelo de formulário em uma pasta e abra o arquivo template.xml em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="e5126-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="e5126-138">Crie e salve um arquivo com a mesma estrutura template.xml com os dados de exemplo que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="e5126-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="e5126-139">Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="e5126-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="e5126-140">Clique na categoria **Visualização** da caixa **de** diálogo Opções de Formulário e, em Exemplo de Dados, especifique o arquivo de dados de exemplo que você criou na caixa **Local do** arquivo. </span><span class="sxs-lookup"><span data-stu-id="e5126-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="e5126-141">Especificando uma função de usuário a ser usada durante a depuração ou visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="e5126-142">Se o formulário com o qual você está trabalhando tiver funções de usuário definidas para ele, você poderá especificar uma função de usuário a ser usada durante a depuração ou visualização do formulário.</span><span class="sxs-lookup"><span data-stu-id="e5126-142">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form.</span></span> <span data-ttu-id="e5126-143">Para obter informações sobre como definir funções de usuário, pesquise a ajuda do InfoPath para "função de usuário".</span><span class="sxs-lookup"><span data-stu-id="e5126-143">For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="e5126-144">A opção para especificar uma função de usuário não estará disponível se a configuração de compatibilidade do seu modelo de formulário estiver definida como Formulário **do Navegador da Web.**</span><span class="sxs-lookup"><span data-stu-id="e5126-144">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**.</span></span> <span data-ttu-id="e5126-145">As funções de usuário não são suportadas em modelos de formulário abertos no navegador do InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="e5126-145">User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="e5126-146">Para especificar uma função a ser usada durante a depuração ou visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="e5126-147">Se você estiver trabalhando no Visual Studio 2012, alternar para o designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e5126-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="e5126-148">Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="e5126-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="e5126-149">Clique na **categoria Visualização** da caixa **de** diálogo Opções de  Formulário e especifique a função de usuário a ser usada na caixa Desv.</span><span class="sxs-lookup"><span data-stu-id="e5126-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="e5126-150">Especificando um domínio a ser usado durante a depuração ou visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="e5126-151">Você pode visualizar um formulário como se ele tivesse sido publicado em um domínio específico.</span><span class="sxs-lookup"><span data-stu-id="e5126-151">You can preview a form as if it was published to a specific domain.</span></span> <span data-ttu-id="e5126-152">Essa configuração só se aplicará se o nível de segurança do modelo de formulário estiver explicitamente definido como **Domínio.**</span><span class="sxs-lookup"><span data-stu-id="e5126-152">This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="e5126-153">Para especificar um domínio a ser usado durante a depuração ou visualização</span><span class="sxs-lookup"><span data-stu-id="e5126-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="e5126-154">Se você estiver trabalhando no Visual Studio 2012, alternar para o designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e5126-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="e5126-155">Clique na guia **Arquivo** e em **Opções de Formulário**. Depois, clique na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="e5126-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="e5126-156">Clique na **categoria Visualização** **da** caixa de diálogo Opções de Formulário e especifique o domínio a ser usado durante a visualização e a depuração na caixa **Domínio.**</span><span class="sxs-lookup"><span data-stu-id="e5126-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="e5126-157">Clique na categoria Segurança  **e** Confiança da caixa  de diálogo Opções de Formulários, des marque a caixa de seleção Determinar automaticamente o nível de segurança e clique em **Domínio.**</span><span class="sxs-lookup"><span data-stu-id="e5126-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

