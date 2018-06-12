---
title: Visualizar e depurar os modelos de formulário do InfoPath com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [InfoPath 2007], modelos de formulário [InfoPath 2007], visualização, depuração [InfoPath 2007], modelos de formulário de código gerenciado, modelos de formulário [InfoPath 2007], depuração, InfoPath 2007, depuração de depuração de visualização modelos de formulário [infopath 2007] modelos de formulário, o InfoPath 2007, visualização de modelos de formulário
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização. Quando você inicia a depuração de código de formulário, o projeto seja compilado e InfoPath exibe seu formulário na janela de visualização do InfoPath. Quando uma linha de código que tem um ponto de interrupção definido para ele for encontrado, o foco é movido para o editor de código. Quando você passar um ponto de interrupção, o foco volta para a janela de visualização. Depuração paradas quando você fecha a janela de visualização.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765609"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="56246-108">Visualizar e depurar os modelos de formulário do InfoPath com código</span><span class="sxs-lookup"><span data-stu-id="56246-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="56246-109">Microsoft InfoPath com o Visual Studio 2012 permite a depuração executando código de formulário no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="56246-109">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode.</span></span> <span data-ttu-id="56246-110">Quando você inicia a depuração de código de formulário, o projeto seja compilado e InfoPath exibe seu formulário na janela de visualização do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56246-110">When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window.</span></span> <span data-ttu-id="56246-111">Quando uma linha de código que tem um ponto de interrupção definido para ele for encontrado, o foco é movido para o editor de código.</span><span class="sxs-lookup"><span data-stu-id="56246-111">When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor.</span></span> <span data-ttu-id="56246-112">Quando você passar um ponto de interrupção, o foco volta para a janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="56246-112">When you continue past a breakpoint, the focus moves back to the preview window.</span></span> <span data-ttu-id="56246-113">Depuração paradas quando você fecha a janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="56246-113">Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="56246-114">Você também pode modificar as opções de formato do modelo de formulário para visualizar e depurar usando uma função de usuário específico, um arquivo de dados de amostra, ou especificando-se o domínio ao qual o formulário será publicado.</span><span class="sxs-lookup"><span data-stu-id="56246-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="56246-115">Não é possível depurar modelos de formulário depois que elas estejam implantadas em tempo de execução do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="56246-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="56246-116">Isso inclui os modelos de formulário que são compatíveis com o InfoPath, bem como aquelas que são compatíveis com o InfoPath e o navegador da Web usando o InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="56246-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="56246-117">No entanto, é possível fazer logon valores de um campo de código em tempo de execução para ajudá-lo com lógica de negócios de um modelo de formulário de depuração.</span><span class="sxs-lookup"><span data-stu-id="56246-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="56246-118">Para obter informações sobre como fazer isso, consulte [Valores de Log para um campo para depuração](how-to-log-values-to-a-field-for-debugging.md).</span><span class="sxs-lookup"><span data-stu-id="56246-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="56246-119">No modo de visualização de depuração</span><span class="sxs-lookup"><span data-stu-id="56246-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="56246-120">Depurar um projeto do InfoPath no modo de visualização</span><span class="sxs-lookup"><span data-stu-id="56246-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="56246-121">Criar ou abrir um modelo de formulário de código gerenciado do InfoPath no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="56246-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="56246-122">Defina um ou mais pontos de interrupção em seu código de formulário no editor de código clicando na barra cinza à esquerda da linha de código onde deseja inserir um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="56246-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="56246-123">Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="56246-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="56246-124">No menu **Depurar** , clique em **Iniciar depuração**; ou pressione F5.</span><span class="sxs-lookup"><span data-stu-id="56246-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="56246-125">O projeto será compilado e o formulário é exibido na janela de visualização.</span><span class="sxs-lookup"><span data-stu-id="56246-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="56246-126">Interagir com o formulário até encontrar uma linha de código que contém um ponto de interrupção.</span><span class="sxs-lookup"><span data-stu-id="56246-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="56246-127">O foco retorna para o editor de código.</span><span class="sxs-lookup"><span data-stu-id="56246-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="56246-128">No menu **Depurar** , clique em **continuar**; ou pressione F5.</span><span class="sxs-lookup"><span data-stu-id="56246-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="56246-129">Quando tiver terminado de depuração, feche a janela de visualização; ou, no menu **Depurar** , clique em **Parar Depuração**.</span><span class="sxs-lookup"><span data-stu-id="56246-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="56246-130">Para depurar um modelo de formulário de código gerenciado do InfoPath ao usar um membro de modelo de objeto que requer confiança total, você deve configurar seu modelo de formulário, conforme descrito em [Visualizar e modelos de formulário de depuração que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="56246-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="56246-131">Usando um arquivo de dados de amostra</span><span class="sxs-lookup"><span data-stu-id="56246-131">Using a Sample Data File</span></span>

<span data-ttu-id="56246-132">Por padrão, a depuração e visualização usa o arquivo de Template. XML que é criado quando um modelo de formulário é criado.</span><span class="sxs-lookup"><span data-stu-id="56246-132">By default, debugging and previewing uses the template.xml file that is created when a form template is created.</span></span> <span data-ttu-id="56246-133">Você pode criar seu próprio arquivo de dados e especificar para usá-la ao visualizar ou depuração usando um dos procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="56246-133">You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="56246-134">Para especificar um arquivo de dados de amostra para usar durante a depuração ou pré-visualizar no Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="56246-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="56246-135">Para exibir Template. XML, abra o modelo de formulário no modo de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="56246-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="56246-136">Clique na guia **arquivo** , clique em **Salvar**, **Salvar o modelo de formulário como**e clique em **Arquivos de origem**.</span><span class="sxs-lookup"><span data-stu-id="56246-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="56246-137">Salvar arquivos de modelo de formulário para uma pasta e abra o arquivo Template. XML em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="56246-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="56246-138">Criar e salvar um arquivo com a mesma estrutura Template. XML com os dados de amostra que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="56246-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="56246-139">Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** .</span><span class="sxs-lookup"><span data-stu-id="56246-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="56246-140">Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e, em seguida, em **dados de amostra** , especifique o arquivo de dados de amostra que você criou na caixa **local do arquivo** .</span><span class="sxs-lookup"><span data-stu-id="56246-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="56246-141">Especificando uma função de usuário para uso durante a depuração ou pré-visualizar</span><span class="sxs-lookup"><span data-stu-id="56246-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="56246-142">Se o formulário que você estiver trabalhando com tem funções de usuário definidas para ele, você poderá especificar uma função de usuário a ser usado durante a depuração ou visualizando o formulário.</span><span class="sxs-lookup"><span data-stu-id="56246-142">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form.</span></span> <span data-ttu-id="56246-143">Para obter informações sobre como definir as funções de usuário, consulte a Ajuda do InfoPath para "função do usuário".</span><span class="sxs-lookup"><span data-stu-id="56246-143">For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="56246-144">A opção para especificar uma função de usuário não estará disponível se a configuração de compatibilidade para o seu modelo de formulário está definida como **Formulário de navegador da Web**.</span><span class="sxs-lookup"><span data-stu-id="56246-144">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**.</span></span> <span data-ttu-id="56246-145">Funções de usuário não são suportadas nos modelos de formulário abertos no navegador do InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="56246-145">User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="56246-146">Para especificar uma função usar durante a depuração ou pré-visualizar</span><span class="sxs-lookup"><span data-stu-id="56246-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="56246-147">Se você estiver trabalhando no Visual Studio 2012, alterne para o InfoPath designer.</span><span class="sxs-lookup"><span data-stu-id="56246-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="56246-148">Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** .</span><span class="sxs-lookup"><span data-stu-id="56246-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="56246-149">Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e especifique a função de usuário para usar na caixa de lista suspensa **Preview como** .</span><span class="sxs-lookup"><span data-stu-id="56246-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="56246-150">A especificação de um domínio para uso durante a depuração ou pré-visualizar</span><span class="sxs-lookup"><span data-stu-id="56246-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="56246-151">Você pode visualizar um formulário como se ele foi publicado para um domínio específico.</span><span class="sxs-lookup"><span data-stu-id="56246-151">You can preview a form as if it was published to a specific domain.</span></span> <span data-ttu-id="56246-152">Essa configuração se aplicará somente se o nível de segurança do modelo de formulário é definido explicitamente como **domínio**.</span><span class="sxs-lookup"><span data-stu-id="56246-152">This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="56246-153">Para especificar um domínio a ser usado durante a depuração ou pré-visualizar</span><span class="sxs-lookup"><span data-stu-id="56246-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="56246-154">Se você estiver trabalhando no Visual Studio 2012, alterne para o InfoPath designer.</span><span class="sxs-lookup"><span data-stu-id="56246-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="56246-155">Clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** .</span><span class="sxs-lookup"><span data-stu-id="56246-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="56246-156">Clique na categoria de **visualização** da caixa de diálogo **Opções de formulário** e, em seguida, especifique o domínio a ser usado durante a visualização e depuração na caixa **domínio** .</span><span class="sxs-lookup"><span data-stu-id="56246-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="56246-157">Clique na categoria de **segurança e confiança** da caixa de diálogo **Opções de formulários** , desmarque a caixa de seleção **determinar automaticamente o nível de segurança** e, em seguida, clique em **domínio**.</span><span class="sxs-lookup"><span data-stu-id="56246-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

