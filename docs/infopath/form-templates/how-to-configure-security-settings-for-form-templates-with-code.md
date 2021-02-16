---
title: Definir configurações de segurança para modelos de formulário com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- pacote de implantação de políticas de segurança [infopath 2007], URLs [InfoPath 2007], atribuição de FullTrust, segurança de acesso ao código [InfoPath 2007], UNCs [InfoPath 2007], atribuição de FullTrust, CAS [InfoPath 2007], segurança [InfoPath 2007], configuração, grupos de código [InfoPath 2007], FullTrust [InfoPath 2007], atribuição a UNCs, FullTrust [InfoPath 2007], atribuição a URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Você pode personalizar o conjunto de permissões aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de Configuração do .NET.
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300153"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="80e98-104">Definir configurações de segurança para modelos de formulário com código</span><span class="sxs-lookup"><span data-stu-id="80e98-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="80e98-105">Você pode personalizar o conjunto de permissões aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de Configuração do .NET.</span><span class="sxs-lookup"><span data-stu-id="80e98-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="80e98-106">A CLR (Common Language Runtime) hospedada pelo InfoPath procurará um grupo de códigos predefinido denominado *Modelos de Formulários do InfoPath* no nível da política de Máquina sob o grupo All_Code.</span><span class="sxs-lookup"><span data-stu-id="80e98-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="80e98-107">A CLR aplicará os conjuntos de permissões definidos nesse grupo ao domínio do aplicativo (AppDomain) no qual o código de formulário é executado.</span><span class="sxs-lookup"><span data-stu-id="80e98-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="80e98-108">Isso permite personalizar os conjuntos de permissões concedidos a modelos de formulário de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="80e98-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="80e98-109">Por exemplo, você pode conceder a permissão para acessar o Active Directory a um modelo de formulário baixado de https://MySite.</span><span class="sxs-lookup"><span data-stu-id="80e98-109">For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="80e98-110">Para que a política de segurança personalizada definida usando o snap-in de Configuração do .NET seja aplicada, ela deve ser implantada em todos os computadores cliente em que o modelo de formulário será executado.</span><span class="sxs-lookup"><span data-stu-id="80e98-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="80e98-111">Para saber mais sobre o modelo de segurança para modelos de formulário de código gerenciado do InfoPath, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="80e98-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="80e98-112">Criar um grupo de códigos para modelos de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="80e98-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="80e98-113">O procedimento a seguir criará um grupo de códigos que não concede permissões a modelos de formulário de código gerenciado do InfoPath (exceto aqueles instalados ou registrados no seu computador local) abaixo do qual você pode atribuir conjuntos de permissões a modelos de formulário do InfoPath localizados em URLs ou UNCs específicos.</span><span class="sxs-lookup"><span data-stu-id="80e98-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="80e98-114">Para saber mais sobre como criar e atribuir conjuntos de permissões a grupos de códigos no grupo de códigos `InfoPath Form Templates`, consulte o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="80e98-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80e98-115">Ao contrário da ferramenta de **Configuração do Microsoft .NET Framework 1.1** instalada com o Pacote Redistribuível do Microsoft .NET Framework 1.1, a ferramenta de **Configuração do Microsoft .NET Framework 2.0** é instalada apenas com o Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="80e98-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="80e98-116">Para criar um grupo de códigos de segurança personalizados para formulários de código gerenciado do InfoPath</span><span class="sxs-lookup"><span data-stu-id="80e98-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="80e98-117">No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="80e98-118">Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="80e98-119">Em **Meu Computador**, expanda o nó **Política de Segurança de Tempo de Execução**, nó **Máquina**, **Grupos de Código**, nó **All_Code** e clique com o botão direito no nó **All_Code** e clique em **Novo** para abrir a caixa de diálogo **Criar Grupo de Códigos**.</span><span class="sxs-lookup"><span data-stu-id="80e98-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="80e98-120">Chame o novo grupo de códigos de `InfoPath Form Templates` (esse texto deve ser exato) e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="80e98-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="80e98-121">Defina o tipo de condição para o grupo de códigos como **Todo o Código** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="80e98-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="80e98-122">Clique em **Usar conjunto de permissões existente**, atribua o conjunto de permissões **Nada** ao grupo de códigos, clique em **Avançar** e depois em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="80e98-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="80e98-123">Para aplicar as novas configurações, feche e reinicie o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="80e98-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="80e98-124">Se preferir, você pode gerenciar o conjunto de permissões para todos os modelos de formulário de código gerenciado do InfoPath, atribuindo um conjunto de permissões diferente de **Nada** ao grupo de códigos **Modelos de Formulário do InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="80e98-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="80e98-125">Você pode alterar o conjunto de permissões para um grupo de códigos de segurança a qualquer momento clicando com o botão direito do mouse no grupo no </span><span class="sxs-lookup"><span data-stu-id="80e98-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="80e98-126">snap-in **Configuração do .NET 2.0**, clicando em **Propriedades** e, em seguida, clicando na guia **Conjunto de Permissões**.</span><span class="sxs-lookup"><span data-stu-id="80e98-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="80e98-127">Atribuição de FullTrust a formulários em uma URL ou UNC específico</span><span class="sxs-lookup"><span data-stu-id="80e98-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="80e98-128">Você pode criar grupos de códigos no grupo **Modelos de Formulário do InfoPath** para conceder o conjunto de permissões de confiança total a modelos de formulário de uma determinada URL ou localização UNC.</span><span class="sxs-lookup"><span data-stu-id="80e98-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="80e98-129">Depois de fazer isso, todos os modelos de formulário publicados na localização especificada serão totalmente confiáveis.</span><span class="sxs-lookup"><span data-stu-id="80e98-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80e98-130">Um modelo de formulário carregado do computador local (grupo de códigos da Zona Meu Computador) é carregado pelo InfoPath usando uma URL aleatória.</span><span class="sxs-lookup"><span data-stu-id="80e98-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="80e98-131">Por esse motivo, você não pode usar o procedimento a seguir para conceder o conjunto de permissões FullTrust a esse modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="80e98-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="80e98-132">Para conceder a um modelo de formulário instalado localmente o conjunto de permissões FullTrust, use um dos procedimentos descritos na seção "Implantação de modelos de formulário que exigem confiança total", no tópico [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="80e98-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="80e98-133">Para atribuir FullTrust a formulários do InfoPath em uma URL ou localização UNC específica</span><span class="sxs-lookup"><span data-stu-id="80e98-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="80e98-134">No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="80e98-135">Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="80e98-136">Em **Meu Computador**, expanda o nó **Política de Segurança de Tempo de Execução**, o nó **Máquina**, o nó **Grupos de Código**, o nó **All_Code** e clique no nó **Modelos de Formulário do InfoPath**.</span><span class="sxs-lookup"><span data-stu-id="80e98-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="80e98-137">Na lista de **Tarefas** do painel direito, clique em **Adicionar um Grupo de Códigos Filho**, nomeie esse grupo de códigos e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="80e98-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="80e98-138">Na lista **Escolha o tipo de condição para este grupo de códigos**, selecione **URL** e insira a URL ou o UNC para a localização dos modelos de formulário de código gerenciado do InfoPath aos quais você deseja conceder o conjunto de permissões **FullTrust**.</span><span class="sxs-lookup"><span data-stu-id="80e98-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="80e98-139">Para restringir o conjunto de permissões a um único modelo de formulário, especifique o caminho completo desse modelo de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="80e98-139">To restrict the permission set to a single form template, specify the full path of that particular form template.</span></span> <span data-ttu-id="80e98-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="80e98-140">For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="80e98-141">Para conceder o conjunto de permissões a todos os modelos de formulário em uma URL ou um UNC, omita o nome do modelo e adicione um asterisco ao final da URL ou do UNC.</span><span class="sxs-lookup"><span data-stu-id="80e98-141">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC.</span></span> <span data-ttu-id="80e98-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="80e98-142">For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="80e98-143">Clique em **Avançar** e, em seguida, clique em **Usar conjunto de permissões existente** e atribua o conjunto de permissões **FullTrust** ao grupo de códigos.</span><span class="sxs-lookup"><span data-stu-id="80e98-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="80e98-144">Clique em **Avançar** e em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="80e98-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="80e98-145">Para aplicar as novas configurações, feche e reinicie o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="80e98-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="80e98-146">Para aplicar um conjunto de permissões mais restritivo ou personalizado, selecione a opção apropriada em vez de **FullTrust** na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="80e98-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="80e98-147">Criação de um pacote de implantação para uma política de segurança do InfoPath</span><span class="sxs-lookup"><span data-stu-id="80e98-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="80e98-148">Depois de definir a política de segurança personalizada para modelos de formulário gerenciado do InfoPath, você pode criar um Pacote do Windows Installer (.msi) para implantar essa política de segurança nos computadores dos usuários, usando a Política de Grupo ou o Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="80e98-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="80e98-149">Para criar um pacote de implantação para uma política de segurança personalizada do InfoPath</span><span class="sxs-lookup"><span data-stu-id="80e98-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="80e98-150">No menu **Iniciar**, aponte para **Ferramentas Administrativas** e clique em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="80e98-151">Se você não tiver **Ferramentas Administrativas** no menu **Iniciar**, no **Painel de Controle**, abra **Ferramentas Administrativas** e clique duas vezes em **Configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="80e98-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="80e98-152">Clique com o botão direito do mouse em **Política de Segurança de Tempo de Execução** e depois clique em **Criar Pacote de Implantação**.</span><span class="sxs-lookup"><span data-stu-id="80e98-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="80e98-153">Em **Selecione a política de segurança a ser implantada**, clique em **Máquina**, especifique a pasta e o nome do arquivo do Pacote do Windows Installer e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="80e98-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="80e98-154">Clique em **Concluir** para criar o pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="80e98-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="80e98-155">Para saber mais sobre como usar a ferramenta de Configuração do .NET Framework, procure "Ferramenta de Configuração do .NET Framework (Mscorcfg.msc)" na Ajuda do Visual Studio ou no site da MSDN.</span><span class="sxs-lookup"><span data-stu-id="80e98-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80e98-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="80e98-156">See also</span></span>



[<span data-ttu-id="80e98-157">Sobre o modelo de segurança para modelos de formulário com código</span><span class="sxs-lookup"><span data-stu-id="80e98-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

