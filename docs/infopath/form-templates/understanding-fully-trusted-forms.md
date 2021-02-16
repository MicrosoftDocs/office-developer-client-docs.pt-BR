---
title: Compreender formulários totalmente confiáveis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são formulários com mais permissões de segurança e que podem acessar outros recursos do sistema e outros componentes no computador de um usuário. Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado, e também como criar um formulário totalmente confiável convertendo manualmente e registrando um formulário padrão, ou então assinando digitalmente um formulário padrão.
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430389"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="052df-104">Compreender formulários totalmente confiáveis</span><span class="sxs-lookup"><span data-stu-id="052df-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="052df-105">InfoPath fornece a capacidade de criar formulários totalmente confiáveis, que são formulários com mais permissões de segurança e que podem acessar outros recursos do sistema e outros componentes no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="052df-105">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer.</span></span> <span data-ttu-id="052df-106">Este artigo descreve o que é um formulário totalmente confiável e por que ele é usado, e também como criar um formulário totalmente confiável convertendo manualmente e registrando um formulário padrão, ou então assinando digitalmente um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="052df-106">This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="052df-107">Os modelos de formulário do InfoPath podem ser implantados com níveis variáveis de segurança.</span><span class="sxs-lookup"><span data-stu-id="052df-107">InfoPath form templates can be deployed with varying levels of security.</span></span> <span data-ttu-id="052df-108">O nível que você usa é determinado pelo nível de acesso a recursos externos que você deseja que o formulário tenha.</span><span class="sxs-lookup"><span data-stu-id="052df-108">The level you use is dictated by the level of access to external resources that you want a form to have.</span></span> <span data-ttu-id="052df-109">Por padrão, os modelos de formulário do InfoPath têm permissão para acessar recursos do sistema e não têm permissão para usar os componentes de software que não são marcados como confiáveis quanto a scripts.</span><span class="sxs-lookup"><span data-stu-id="052df-109">By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting.</span></span> <span data-ttu-id="052df-110">No entanto, esse comportamento pode ser substituído para que um formulário possa acessar recursos do sistema e outros recursos externos, incluindo componentes de software que não são marcados como confiáveis quanto a scripts.</span><span class="sxs-lookup"><span data-stu-id="052df-110">However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="052df-111">Para que um formulário seja usado, o InfoPath deve ser capaz de acessar o modelo de formulário em que o formulário se baseia.</span><span class="sxs-lookup"><span data-stu-id="052df-111">For a form to be used, InfoPath must be able to access the form template that the form is based on.</span></span> <span data-ttu-id="052df-112">Quando você cria um modelo de formulário, o InfoPath cria uma entrada no arquivo de definição de formulário (.xsf) que contém a URL da localização do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-112">When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template.</span></span> <span data-ttu-id="052df-113">Um formulário baseado em URL é denominado como *de área restrita*.</span><span class="sxs-lookup"><span data-stu-id="052df-113">A URL-based form is said to be *sandboxed*.</span></span> <span data-ttu-id="052df-114">Quando um usuário o preencher, o formulário será adicionado a um cache local e seu acesso a recursos do sistema será negado.</span><span class="sxs-lookup"><span data-stu-id="052df-114">When a user fills it out, the form is added in a local cache and denied access to system resources.</span></span> <span data-ttu-id="052df-115">Esse tipo de formulário herda suas permissões do domínio no qual é aberto.</span><span class="sxs-lookup"><span data-stu-id="052df-115">This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="052df-116">No entanto, você pode modificar um formulário para que ele seja baseado em um Nome de recurso Uniforme (URN), que permite acesso aos recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="052df-116">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources.</span></span> <span data-ttu-id="052df-117">Os formulários desse tipo são considerados *totalmente confiáveis*.</span><span class="sxs-lookup"><span data-stu-id="052df-117">Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="052df-118">Por que usar um Formulário Totalmente Confiável?</span><span class="sxs-lookup"><span data-stu-id="052df-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="052df-119">Os formulários totalmente confiáveis têm um melhor conjunto de permissões do que os formulários de área restrita.</span><span class="sxs-lookup"><span data-stu-id="052df-119">Fully trusted forms have a better set of permissions than sandboxed forms.</span></span> <span data-ttu-id="052df-120">Por exemplo, podem conter o código de programação que usa objetos externos para acessar recursos do sistema, podem usar componentes de software ou os controles do Microsoft ActiveX não marcados como confiáveis para scripts, e podem usar a lógica de negócios personalizados fornecida pelas assemblies do .NET.</span><span class="sxs-lookup"><span data-stu-id="052df-120">For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="052df-121">Além disso, alguns membros do modelo de objeto do InfoPath estão definidos para o nível de segurança 3, o que significa que só podem ser usados em um formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-121">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form.</span></span> <span data-ttu-id="052df-122">Por exemplo, para acessar o objeto **CommandBars** do Microsoft Office, você usa a propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) do InfoPath para definir uma referência para ele.</span><span class="sxs-lookup"><span data-stu-id="052df-122">For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it.</span></span> <span data-ttu-id="052df-123">Como esta propriedade está configurada com o nível de segurança 3, ela não pode ser usada em um formulário que não é totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-123">Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="052df-124">O uso da propriedade [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) da classe [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx), ou qualquer outro membro de modelo de objeto com nível de segurança 3, em um formulário que não seja totalmente confiável resultará em um erro de “permissão negada”.</span><span class="sxs-lookup"><span data-stu-id="052df-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="052df-125">O que torna um formulário totalmente confiável?</span><span class="sxs-lookup"><span data-stu-id="052df-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="052df-126">As seguintes ações, que estão envolvidas tanto na interface do usuário do InfoPath quanto nos arquivos de formulário, são requeridas para criar e usar um formulário totalmente confiável:</span><span class="sxs-lookup"><span data-stu-id="052df-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="052df-127">Habilitar o InfoPath para permitir o uso de formulários totalmente confiáveis na categoria **Editores Confiáveis** da caixa de diálogo **Central de Confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="052df-127">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="052df-128">Esta opção deve ser habilitada para que os usuários abram formulários totalmente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="052df-128">This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="052df-129">Registrar o formulário totalmente confiável no computador de destino usando o método **RegisterSolution** do objeto **Application** do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="052df-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="052df-130">Criar um Formulário Totalmente Confiável</span><span class="sxs-lookup"><span data-stu-id="052df-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="052df-131">Você pode criar o formulário manualmente, o que envolve modificar diretamente alguns arquivos de formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="052df-132">Você pode assinar digitalmente o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="052df-133">Criar um Formulário Totalmente Confiável manualmente</span><span class="sxs-lookup"><span data-stu-id="052df-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="052df-134">Para criar manualmente um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="052df-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="052df-135">Fazer uma cópia de backup do modelo de formulário que você deseja tornar totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="052df-136">Abra o modelo de formulário no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="052df-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="052df-137">Salve os arquivos de origem dos formulários em uma pasta em seu disco rígido, clicando na guia **Arquivo**, clicando em **Publicar** e depois em **Exportar arquivos de origem**.</span><span class="sxs-lookup"><span data-stu-id="052df-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="052df-138">Especifique a pasta onde deseja salvar os arquivos de origem dos formulários, clique em **OK** e saia do InfoPath Designer.</span><span class="sxs-lookup"><span data-stu-id="052df-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="052df-139">Na pasta onde os arquivos de formulário foram extraídos, abra o arquivo de definição de formulário (.xsf), nomeado `manifest.xsf` por padrão, em um editor de texto como o Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="052df-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="052df-140">Adicione os atributos de seguir ao elemento **xDocumentClass** no arquivo. xsf:</span><span class="sxs-lookup"><span data-stu-id="052df-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > Os valores que são usados para a URN podem ser qualquer tipo de valor de cadeia de caracteres, desde que esse valor seja único. Deve haver pelo menos dois valores após o prefixo `urn:`, e esses valores devem ser separados por um ponto-e-vírgula. <span data-ttu-id="052df-143">Além disso, a URN não deve exceder 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="052df-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="052df-144">Salve e feche o arquivo. xsf e depois abra o arquivo do modelo XML (.xml), que é nomeado `Template.xml` por padrão, em um editor de texto como o Notepad.</span><span class="sxs-lookup"><span data-stu-id="052df-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="052df-145">Remova o atributo **href** da instrução de processamento `mso-infoPathSolution` e substitua-o pelo mesmo atributo **name** que você usou na etapa 6 para o arquivo .xsf.</span><span class="sxs-lookup"><span data-stu-id="052df-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="052df-146">Os valores URN usados para o atributo **name** devem ser os mesmos no arquivo .xsf e no arquivo do modelo XML.</span><span class="sxs-lookup"><span data-stu-id="052df-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="052df-147">Salve e feche o arquivo de modelo XML.</span><span class="sxs-lookup"><span data-stu-id="052df-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="052df-148">Reempacote os arquivos em um formato CAB .xsn com uma ferramenta como makecab.exe.</span><span class="sxs-lookup"><span data-stu-id="052df-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="052df-149">Embora o designer de formulários do InfoPath suporte o reempacotamento de arquivos de formulário em um arquivo .xsn existente, essa ação reverte o formulário para um formulário baseado em URL.</span><span class="sxs-lookup"><span data-stu-id="052df-149">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form.</span></span> <span data-ttu-id="052df-150">Por esse motivo, você deve reempacotar os arquivos manualmente para evitar substituir suas alterações nos arquivos de formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-150">For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="052df-151">Crie uma programa de instalação personalizado usando o método **RegisterSolution** do objeto **Application** do InfoPath para instalar o formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-151">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form.</span></span> <span data-ttu-id="052df-152">Uma maneira simples de fazer isso é criar um arquivo de script que usa as linhas seguintes de código (na sintaxe Microsoft JScript ou VBScript):</span><span class="sxs-lookup"><span data-stu-id="052df-152">A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
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
> <span data-ttu-id="052df-153">Embora este exemplo use um arquivo de script simples, você também pode usar um mecanismo de instalação mais robusto como arquivos Microsoft Windows Installer (.msi).</span><span class="sxs-lookup"><span data-stu-id="052df-153">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files.</span></span> <span data-ttu-id="052df-154">Certifique-se, no entanto, de usar o método **RegisterSolution** para instalar corretamente o formulário totalmente confiável no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="052df-154">Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer.</span></span> <span data-ttu-id="052df-155">Para acessar o método **RegisterSolution** do objeto **Application** do InfoPath a partir do Visual Basic ou do Visual Studio, defina uma referência na biblioteca de tipos do Microsoft InfoPath 3.0, que é fornecida pelo IPEDITOR.dll instalado em C:\Arquivos de Programas\Microsoft Office\Office14.</span><span class="sxs-lookup"><span data-stu-id="052df-155">To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="052df-156">Se você precisar remover um formulário totalmente confiável, pode usar o método **UnregisterSolution** do objeto **Application**, como mostrado nos seguintes exemplos de JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="052df-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
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

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="052df-157">Assinar digitalmente um modelo de formulário para criar um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="052df-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="052df-158">Assinar digitalmente um modelo de formulário permite que você implante um modelo de formulário totalmente confiável por email ou em um servidor Web, como um servidor executando o Microsoft SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="052df-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="052df-159">Use as etapas dos três procedimentos seguintes para fazer um formulário totalmente confiável especificando confiabilidade total para o formulário, assinando-o digitalmente e depois publicando-o.</span><span class="sxs-lookup"><span data-stu-id="052df-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="052df-160">Para assinar digitalmente um modelo de formulário</span><span class="sxs-lookup"><span data-stu-id="052df-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="052df-161">Abra o formulário no designer do InfoPath, clique na guia **Arquivo** e, em seguida, em **Opções de Formulário** na guia **Informações**.</span><span class="sxs-lookup"><span data-stu-id="052df-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="052df-162">Na caixa de diálogo **Opções de Formulário**, clique na categoria **Segurança e Confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="052df-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="052df-163">Desmarque a caixa de seleção **Determinar automaticamente o nível de segurança (recomendado)**.</span><span class="sxs-lookup"><span data-stu-id="052df-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="052df-164">Selecione **Confiabilidade Total (o formulário tem acesso a arquivos e configurações do computador do usuário)**.</span><span class="sxs-lookup"><span data-stu-id="052df-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="052df-165">Em **Assinatura do Modelo de Formulário**, selecione **Assinar este modelo de formulário**.</span><span class="sxs-lookup"><span data-stu-id="052df-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="052df-166">Clique em **Selecionar Certificado** para selecionar um certificado foi baixado e instalado anteriormente de um provedor de certificação confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="052df-167">Clique duas vezes em OK para sair totalmente.</span><span class="sxs-lookup"><span data-stu-id="052df-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="052df-168">Para publicar o modelo de formulário em uma biblioteca de documentos do SharePoint</span><span class="sxs-lookup"><span data-stu-id="052df-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="052df-169">Clique na guia **Arquivo**, clique em **Publicar** e em **SharePoint Server**.</span><span class="sxs-lookup"><span data-stu-id="052df-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="052df-170">Siga as instruções do **Assistente de publicação** para publicar o modelo de formulário em uma biblioteca de documentos nova ou existente do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="052df-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="052df-171">Para criar um formulário baseado no modelo de formulário totalmente confiável assinado digitalmente</span><span class="sxs-lookup"><span data-stu-id="052df-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="052df-172">Na biblioteca de documentos do SharePoint, clique em **Preencher o formulário**.</span><span class="sxs-lookup"><span data-stu-id="052df-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="052df-173">Depois de publicar o modelo de formulário para uma biblioteca de documentos do SharePoint usando o **Assistente de publicação**, o modelo não será exibido como um item na biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="052df-173">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library.</span></span> <span data-ttu-id="052df-174">Quando você cria um formulário nessa biblioteca de documentos, o modelo será usado por padrão como o modelo para o novo formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-174">When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="052df-175">Se o modelo de formulário padrão foi assinado digitalmente, o InfoPath exibe um aviso de segurança sobre o modelo de formulário assinado digitalmente.</span><span class="sxs-lookup"><span data-stu-id="052df-175">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template.</span></span> <span data-ttu-id="052df-176">Selecione **Sempre confiar em arquivos deste editor e abri-los automaticamente** e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="052df-176">Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="052df-177">Usar um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="052df-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="052df-178">Usar um formulário totalmente confiável é muito semelhante a usar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="052df-178">Using a fully trusted form is very similar to using a standard form.</span></span> <span data-ttu-id="052df-179">As únicas diferenças significativas são que o formulário pode acessar recursos restritos e que avisos não serão mais exibidos.</span><span class="sxs-lookup"><span data-stu-id="052df-179">The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="052df-180">Para habilitar o InfoPath a usar um formulário totalmente confiável, os usuários devem garantir que a caixa de seleção **Permitir a execução de formulários totalmente confiáveis em meu computador** esteja selecionada na categoria **Editores Confiáveis** da caixa de diálogo **Central de Confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="052df-180">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box.</span></span> <span data-ttu-id="052df-181">Para abrir a caixa de diálogo **Central de Confiabilidade**, clique na guia **Arquivo**, clique em **Opções** (abaixo da guia **InfoPath**), clique em **Central de Confiabilidade** e depois em **Configurações da Central de Confiabilidade**.</span><span class="sxs-lookup"><span data-stu-id="052df-181">To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="052df-182">Um formulário totalmente confiável pode ser aberto no InfoPath a partir da caixa de diálogo **Preencher um formulário**.</span><span class="sxs-lookup"><span data-stu-id="052df-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="052df-183">A caixa de diálogo **Preencher um formulário** se abre quando você clica em **Mais Formulários** no painel de tarefas **Preencher um formulário**, ou quando você clica em **Preencher um formulário** no menu **Arquivo**.</span><span class="sxs-lookup"><span data-stu-id="052df-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="052df-184">Fazer alterações em um formulário totalmente confiável</span><span class="sxs-lookup"><span data-stu-id="052df-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="052df-185">Se você precisar fazer alterações apenas em um arquivo .xsn, pode fazer com que os usuários substituam seu arquivo .xsn existente pelo novo arquivo depois que as alterações forem feitas.</span><span class="sxs-lookup"><span data-stu-id="052df-185">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made.</span></span> <span data-ttu-id="052df-186">Eles não precisarão reinstalá-lo usando um programa de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="052df-186">They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="052df-187">Porém, se você estiver fazendo alterações em arquivos de formulário que o arquivo .xsn contém, vai precisar reempacotar os arquivos, como explicado anteriormente, e depois fazer com que os usuários reinstalem o formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="052df-188">A melhor abordagem é salvar o modelo de formulário de volta no formato .xsn do designer do InfoPath e depois seguir as etapas deste artigo para criar um formulário totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="052df-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="052df-189">Conclusão</span><span class="sxs-lookup"><span data-stu-id="052df-189">Conclusion</span></span>

<span data-ttu-id="052df-190">Dependendo dos requisitos de seu negócio e das necessidades dos seus usuários, você pode precisar criar um formulário com um conjunto de permissões mais elevado do que o formulário padrão do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="052df-190">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form.</span></span> <span data-ttu-id="052df-191">O InfoPath proporciona a capacidade de modificar um formulário de forma que ele possa acessar recursos do sistema e outros recursos externos não marcados como confiáveis quanto a script.</span><span class="sxs-lookup"><span data-stu-id="052df-191">InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting.</span></span> <span data-ttu-id="052df-192">Isso pode ser feito manualmente, fazendo modificações nos arquivos de formulário que um modelo de formulário contém e executando um script de instalação, ou então assinando digitalmente o modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="052df-192">This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

