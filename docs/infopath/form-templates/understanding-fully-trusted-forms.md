---
title: Noções básicas sobre totalmente formulários confiáveis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: O InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são os formulários que possui permissões de segurança maiores e podem acessar recursos do sistema e outros componentes no computador de um usuário. Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado e criar um formulário totalmente confiável manualmente convertendo e registrando um formulário padrão ou ao assinar digitalmente um formulário padrão.
ms.openlocfilehash: b410d5bee0080aae5e0af9687999595655b42edf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765710"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="5d7e3-104">Noções básicas sobre totalmente formulários confiáveis</span><span class="sxs-lookup"><span data-stu-id="5d7e3-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="5d7e3-105">O InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são os formulários que possui permissões de segurança maiores e podem acessar recursos do sistema e outros componentes no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="5d7e3-106">Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado e criar um formulário totalmente confiável manualmente convertendo e registrando um formulário padrão ou ao assinar digitalmente um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="5d7e3-107">Modelos de formulário do InfoPath podem ser implantados com vários níveis de segurança.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-107">InfoPath form templates can be deployed with varying levels of security.</span></span> <span data-ttu-id="5d7e3-108">O nível que você use é determinado pelo nível de acesso aos recursos externos que você deseja que tenham um formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-108">The level you use is dictated by the level of access to external resources that you want a form to have.</span></span> <span data-ttu-id="5d7e3-109">Por padrão, os modelos de formulário do InfoPath são impedidos de acessar os recursos do sistema e não têm permissão para usar quaisquer componentes de software que não são marcados como seguros para script.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-109">By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting.</span></span> <span data-ttu-id="5d7e3-110">No entanto, esse comportamento pode ser substituído para que um formulário possa acessar recursos do sistema e outros recursos externos, incluindo os componentes de software que não são marcados como seguros para script.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-110">However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="5d7e3-111">Para um formulário a ser usado, o InfoPath deve ser capaz de acessar o modelo de formulário para o qual o formulário se baseia.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-111">For a form to be used, InfoPath must be able to access the form template that the form is based on.</span></span> <span data-ttu-id="5d7e3-112">Quando você cria um modelo de formulário, o InfoPath cria uma entrada no arquivo de definição (. xsf) do formulário que contém a URL do local do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-112">When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template.</span></span> <span data-ttu-id="5d7e3-113">Um formulário baseado em URL será considerado *em área restrita*.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-113">A URL-based form is said to be *sandboxed*.</span></span> <span data-ttu-id="5d7e3-114">Quando o usuário preenche-out, o formulário é adicionado em um cache local e acesso negado aos recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-114">When a user fills it out, the form is added in a local cache and denied access to system resources.</span></span> <span data-ttu-id="5d7e3-115">Esse tipo de formulário herda suas permissões do domínio no qual ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-115">This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="5d7e3-116">No entanto, você pode modificar um formulário para que ele se baseia em um recurso URN (nome) em vez disso, que permite acesso aos recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-116">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources.</span></span> <span data-ttu-id="5d7e3-117">Formulários desse tipo são considerados *totalmente confiáveis*.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-117">Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-118">Por que usar um formulário totalmente confiável?</span><span class="sxs-lookup"><span data-stu-id="5d7e3-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="5d7e3-119">Formulários totalmente confiáveis têm um conjunto melhor de permissões de formulários em área restrita.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-119">Fully trusted forms have a better set of permissions than sandboxed forms.</span></span> <span data-ttu-id="5d7e3-120">Por exemplo, eles podem conter o código de programação que utiliza objetos externos para acessar os recursos do sistema, eles podem usar os componentes de software ou os controles Microsoft ActiveX não marcados como seguros para script e eles podem usar a lógica de negócios personalizado fornecida pelo. Assemblies do NET.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-120">For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="5d7e3-121">Além disso, a alguns membros do modelo de objeto do InfoPath são definidos com o nível de segurança 3, que significa que eles só podem ser usados em um formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-121">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form.</span></span> <span data-ttu-id="5d7e3-122">Por exemplo, para acessar o objeto do Microsoft Office **CommandBars** , use a propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe InfoPath [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) para definir uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-122">For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it.</span></span> <span data-ttu-id="5d7e3-123">Porque essa propriedade é definida para o nível de segurança 3, ele não pode ser usado em um formulário que não seja totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-123">Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5d7e3-124">Usando a propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe da [janela](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ou qualquer outro membro de modelo de objeto que tem um nível de segurança de 3, em um formulário que não seja totalmente confiável resultará em um erro "permission denied".</span><span class="sxs-lookup"><span data-stu-id="5d7e3-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="5d7e3-125">O que torna um formulário totalmente confiável?</span><span class="sxs-lookup"><span data-stu-id="5d7e3-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="5d7e3-126">As seguintes ações, envolvendo tanto a interface de usuário do InfoPath e os arquivos de formulário são necessários para criar e usar um formulário totalmente confiável:</span><span class="sxs-lookup"><span data-stu-id="5d7e3-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="5d7e3-127">Habilitando o InfoPath permitir o uso de formulários totalmente confiáveis na categoria **Editores confiáveis** da caixa de diálogo **Central de confiabilidade** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-127">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="5d7e3-128">Esta opção deve ser habilitada para os usuários abram formulários totalmente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-128">This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="5d7e3-129">Registrando o formulário totalmente confiável no computador de destino usando o método **RegisterSolution** do objeto do InfoPath **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-130">Criação de um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="5d7e3-131">Você pode criar o formulário manualmente, que envolve a modificação de alguns dos arquivos formulário diretamente.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="5d7e3-132">Você pode assinar digitalmente o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-133">Criar manualmente um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-134">Criar manualmente um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="5d7e3-135">Faça uma cópia de backup do modelo de formulário que você deseja tornar totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="5d7e3-136">Abra o modelo de formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="5d7e3-137">Salve o formulário arquivos de origem em uma pasta no seu disco rígido clicando na guia **arquivo** , clicando em **Publish**, e clicando em **Exportar arquivos de origem**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="5d7e3-138">Especifique a pasta na qual deseja salvar o formulário arquivos de origem, clique em **Okey**e saia do InfoPath designer.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="5d7e3-139">Na pasta em que você extraiu os arquivos de formulário, abra o arquivo de definição (. xsf) do formulário, chamado `manifest.xsf` por padrão, em um editor de texto como o Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="5d7e3-140">Adicione os seguintes atributos ao elemento **xDocumentClass** no arquivo. xsf:</span><span class="sxs-lookup"><span data-stu-id="5d7e3-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Os valores que são usados para o URN podem ser qualquer tipo de valor de cadeia de caracteres, desde que esse valor for exclusivo. Deve haver pelo menos dois valores após o `urn:` prefixo e esses valores devem ser separados por dois pontos. <span data-ttu-id="5d7e3-143">Além disso, o URN não deve exceder 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="5d7e3-144">Salve e feche o arquivo. xsf e abra o arquivo de modelo (. xml) do XML nomeado `Template.xml` por padrão, em um editor de texto como o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="5d7e3-145">Remova o atributo **href** do `mso-infoPathSolution` instrução de processamento e substituí-lo com o mesmo atributo de **nome** que você usou na etapa 6 para o arquivo. xsf.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="5d7e3-146">Os valores URN que são usados para o atributo **name** devem ser o mesmo no arquivo. xsf tanto arquivo de modelo XML.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="5d7e3-147">Salve e feche o arquivo de modelo XML.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="5d7e3-148">Remonte os arquivos no formato. xsn CAB com uma ferramenta como makecab.exe.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="5d7e3-149">Embora o designer de formulários do InfoPath suporta remontagem os arquivos de formulário em um arquivo. xsn, fazer isso reverterá o formulário a um formulário baseado em URL.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-149">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form.</span></span> <span data-ttu-id="5d7e3-150">Por esse motivo, você deve remonte os arquivos manualmente para evitar sobrescrever as alterações nos arquivos de formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-150">For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="5d7e3-151">Crie um programa de instalação personalizada usando o método **RegisterSolution** do objeto do InfoPath **aplicativo** para instalar o formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-151">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form.</span></span> <span data-ttu-id="5d7e3-152">Uma maneira simples de fazer isso é criar um arquivo de script que usa as seguintes linhas de código (em sintaxe Microsoft JScript ou VBScript):</span><span class="sxs-lookup"><span data-stu-id="5d7e3-152">A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> <span data-ttu-id="5d7e3-153">Embora este exemplo usa um arquivo de script simples, você também pode usar um mecanismo de instalação mais robusto como arquivos do Microsoft Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="5d7e3-153">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files.</span></span> <span data-ttu-id="5d7e3-154">Certifique-se, no entanto, usar o método **RegisterSolution** para instalar corretamente o formulário totalmente confiável no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-154">Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer.</span></span> <span data-ttu-id="5d7e3-155">Para acessar o método **RegisterSolution** do objeto **Application** do InfoPath no Visual Basic ou Visual Studio, defina uma referência à biblioteca de tipos do Microsoft InfoPath 3.0, fornecida pelo IPEDITOR.dll que é instalado na C:\Program Pasta Files\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-155">To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="5d7e3-156">Se você tiver que remover um formulário totalmente confiável, você pode usar o método **UnregisterSolution** do objeto **Application** , conforme mostrado nos exemplos a seguir JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-157">Assinar digitalmente um modelo de formulário para criar um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="5d7e3-158">Assinar digitalmente um modelo de formulário permite implantar um modelo de formulário totalmente confiável por email ou em um servidor Web, como um servidor que está executando o Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="5d7e3-159">Use as etapas nos seguintes três procedimentos para tornar um formulário totalmente confiável especificando confiança total para o formulário, assiná-lo digitalmente e, em seguida, publicá-lo.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="5d7e3-160">Para assinar digitalmente um modelo de formulário</span><span class="sxs-lookup"><span data-stu-id="5d7e3-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="5d7e3-161">Abra o formulário no InfoPath designer, clique na guia **arquivo** e clique em **Opções de formulário** , na guia **informações** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="5d7e3-162">Na caixa de diálogo **Opções de formulário** , clique na categoria de **segurança e confiança** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="5d7e3-163">Desmarque a seleção para **determinar o nível de segurança automaticamente (recomendado)**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="5d7e3-164">Selecione a **Confiança total (o formulário tem acesso aos arquivos e configurações no computador do usuário)**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="5d7e3-165">Em **Assinatura do modelo de formulário**, selecione **o modelo de formulário de entrada**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="5d7e3-166">Clique em **Selecionar certificado** para selecionar um certificado que foi baixado e instalado a partir de um provedor de certificado confiável anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="5d7e3-167">Clique duas vezes em Okey para sair completamente.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="5d7e3-168">Para publicar o modelo de formulário em uma biblioteca de documentos do SharePoint</span><span class="sxs-lookup"><span data-stu-id="5d7e3-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="5d7e3-169">Clique na guia **arquivo** , clique em **Publicar**e, em seguida, clique em **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="5d7e3-170">Siga as instruções no **Assistente de publicação** para publicar o modelo de formulário em uma biblioteca de documentos nova ou existente do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="5d7e3-171">A um criar um formulário baseado no modelo de formulário totalmente confiável, digitalmente assinadas</span><span class="sxs-lookup"><span data-stu-id="5d7e3-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="5d7e3-172">Na biblioteca de documentos do SharePoint, clique em **Preencher o formulário**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="5d7e3-173">Depois de publicar o modelo de formulário para uma biblioteca de documentos do SharePoint usando o **Assistente de publicação**, o modelo não será exibido como um item na biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-173">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library.</span></span> <span data-ttu-id="5d7e3-174">Quando você cria um formulário nessa biblioteca de documentos, o modelo será usado por padrão como o modelo para o novo formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-174">When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="5d7e3-175">Se o modelo de formulário padrão foi assinado digitalmente, o InfoPath exibirá um aviso de segurança sobre o modelo de formulário assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-175">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template.</span></span> <span data-ttu-id="5d7e3-176">Selecione **Sempre confiar em arquivos deste editor e abri-los automaticamente**e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-176">Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-177">Usando um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="5d7e3-178">O uso de um formulário totalmente confiável é muito semelhante ao uso de um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-178">Using a fully trusted form is very similar to using a standard form.</span></span> <span data-ttu-id="5d7e3-179">As diferenças apenas significativas são que o formulário pode acessar recursos restritos e avisos não serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-179">The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d7e3-180">Para habilitar o InfoPath, para usar um formulário totalmente confiável, os usuários devem assegurar que a caixa de seleção **Permitir que formulários completamente confiáveis sejam executados no meu computador** é selecionada na categoria **Editores confiáveis** da caixa de diálogo **Central de confiabilidade** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-180">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="5d7e3-181">Para abrir a caixa de diálogo **Central de confiabilidade** , clique na guia **arquivo** , clique em **Opções** (abaixo da guia **InfoPath** ), clique em **Central de confiabilidade**e, em seguida, clique em **Configurações da Central de confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-181">To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="5d7e3-182">Um formulário totalmente confiável pode ser aberto no InfoPath da caixa de diálogo **Preencher um formulário** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="5d7e3-183">A caixa de diálogo **Preencher um formulário** é aberto quando você clicar em **Mais formulários** no painel de tarefas **Preencher um formulário** , ou clique em **Preencher um formulário** , no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="5d7e3-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="5d7e3-184">Fazendo alterações em um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="5d7e3-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="5d7e3-185">Se você precisar fazer alterações no arquivo. xsn, você pode ter usuários substitua seu arquivo. xsn existente uma nova depois que as alterações forem feitas.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-185">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made.</span></span> <span data-ttu-id="5d7e3-186">Eles não terão reinstalá-lo usando um programa de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-186">They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="5d7e3-187">No entanto, se você estiver fazendo alterações para os arquivos de formulário que contém o arquivo. xsn, você deve remonte os arquivos, conforme explicado anteriormente e, em seguida, tiver usuários reinstalar o formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5d7e3-188">A melhor abordagem é salvar o modelo de formulário volta para o formato. xsn do InfoPath designer e siga as etapas neste artigo para criar um formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="5d7e3-189">Conclusion</span><span class="sxs-lookup"><span data-stu-id="5d7e3-189">Conclusion</span></span>

<span data-ttu-id="5d7e3-190">Dependendo de suas necessidades de negócios e as necessidades dos seus usuários, você pode precisar criar um formulário que tenha um conjunto maior de permissões que o formulário padrão do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-190">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form.</span></span> <span data-ttu-id="5d7e3-191">O InfoPath fornece a capacidade de modificar um formulário para que ele possa acessar os recursos do sistema e outros recursos externos que não são marcados como seguros para script.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-191">InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting.</span></span> <span data-ttu-id="5d7e3-192">Isso pode ser feito manualmente por fazer modificações nos arquivos de formulário que contém um modelo de formulário e executar um script de instalação ou por assinar digitalmente o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="5d7e3-192">This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

