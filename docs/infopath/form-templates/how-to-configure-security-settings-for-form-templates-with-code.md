---
title: Definir configurações de segurança para modelos de formulário com código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- implantação da diretiva de segurança empacotar as URLs de [infopath 2007], [InfoPath 2007], atribuindo FullTrust, código de segurança de acesso [InfoPath 2007], UNCs [InfoPath 2007], atribuindo FullTrust, CAS [InfoPath 2007], [InfoPath 2007] de segurança, configuração, [de grupos de código FullTrust do InfoPath 2007], [InfoPath 2007], atribuindo a UNCs, FullTrust [InfoPath 2007], atribuindo a URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Você pode personalizar o conjunto de permissões que é aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de configuração do .NET.
ms.openlocfilehash: f04ce71875eac7695d2900131ca7c9cd333fa90f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765620"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="d842b-104">Definir configurações de segurança para modelos de formulário com código</span><span class="sxs-lookup"><span data-stu-id="d842b-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="d842b-105">Você pode personalizar o conjunto de permissões que é aplicado a um modelo de formulário de código gerenciado do InfoPath usando o snap-in de configuração do .NET.</span><span class="sxs-lookup"><span data-stu-id="d842b-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="d842b-106">O common language runtime (CLR) hospedado pelo InfoPath procurará um grupo de código predefinido chamado *Modelos de formulário do InfoPath* no nível de diretiva de máquina sob o grupo All_Code.</span><span class="sxs-lookup"><span data-stu-id="d842b-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="d842b-107">O CLR aplicará os conjuntos de permissões que estão definidos de acordo com esse grupo para o domínio de aplicativo (AppDomain) onde o código do formulário é executado.</span><span class="sxs-lookup"><span data-stu-id="d842b-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="d842b-108">Isso permite que você personalize os conjuntos de permissões são concedidos aos modelos de formulário de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d842b-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="d842b-109">Por exemplo, você pode conceder a um modelo de formulário baixado de http://MySite permissão para acessar o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d842b-109">For example, you can grant a form template downloaded from http://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="d842b-110">Para a diretiva de segurança personalizadas definida usando o snap-in de configuração do .NET a ser aplicado, ele deve ser implantado em todos os computadores cliente onde o modelo de formulário será executado.</span><span class="sxs-lookup"><span data-stu-id="d842b-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="d842b-111">Para obter mais informações sobre o modelo de segurança para o InfoPath gerenciado modelos de formulário de código, consulte [Sobre o modelo de segurança para modelos de formulário com código](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="d842b-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="d842b-112">Criando um grupo de códigos para modelos de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="d842b-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="d842b-113">O procedimento a seguir criará um grupo de código que concede nenhuma permissão ao InfoPath gerenciado código modelos de formulário (exceto aqueles que são instalados ou registrados no computador local) em que você pode atribuir permissão define como modelos de formulário do InfoPath localizados em URLs ou UNCs específico.</span><span class="sxs-lookup"><span data-stu-id="d842b-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="d842b-114">Para obter informações sobre como criar e atribuir permissão define a grupos de código dentro do `InfoPath Form Templates` código grupo, consulte o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="d842b-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d842b-115">Diferentemente da ferramenta de **configuração do Microsoft .NET Framework 1.1** é instalada com o pacote redistribuível do Microsoft .NET Framework 1.1, a **configuração do Microsoft .NET Framework 2.0** é instalado apenas com o Microsoft .NET Framework 2.0 software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d842b-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="d842b-116">Para criar um grupo de códigos de segurança personalizada para o InfoPath gerenciados formulários de código</span><span class="sxs-lookup"><span data-stu-id="d842b-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="d842b-117">No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="d842b-118">Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="d842b-119">Em **Meu computador**, expanda o nó de **Diretiva de segurança de tempo de execução** , o nó de **máquina** , o nó de **Grupos de código** , o nó **All_Code** e com o botão direito no nó **All_Code** e clique em **novo** para abrir o **Create Grupo de códigos** caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d842b-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="d842b-120">Nomeie o novo grupo de código `InfoPath Form Templates` (este texto deve ser exato) e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d842b-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="d842b-121">Definir o tipo de condição para o grupo de código para **Todo o código**e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d842b-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="d842b-122">Clique em **Definir permissão de uso existente**, atribua o conjunto de permissões **Nothing** ao grupo código, clique em **Avançar**e, em seguida, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="d842b-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="d842b-123">Para aplicar as novas configurações, feche e reinicie o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d842b-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="d842b-124">Se você preferir, você pode gerenciar a permissão definida para todos os modelos de formulário de código gerenciado do InfoPath, atribuindo-se um conjunto de permissões que não seja **Nothing** conjunto de permissões para o grupo de códigos de **Modelos de formulário do InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="d842b-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="d842b-125">Você pode alterar a permissão definida para um grupo de segurança de códigos a qualquer momento clicando com o grupo a.</span><span class="sxs-lookup"><span data-stu-id="d842b-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="d842b-126">**NET Configuration 2.0** snap-in, clicando em **Propriedades**e, em seguida, clicando na guia **Permission Set** .</span><span class="sxs-lookup"><span data-stu-id="d842b-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="d842b-127">Atribuindo FullTrust aos formulários em um UNC ou URL específica</span><span class="sxs-lookup"><span data-stu-id="d842b-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="d842b-128">Você pode criar grupos de código sob o grupo de **Modelos de formulário do InfoPath** para conceder a permissão de confiança total definida como modelos de formulário de uma localidade específica de URL ou UNC.</span><span class="sxs-lookup"><span data-stu-id="d842b-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="d842b-129">Depois de fazer isso, cada modelo de formulário publicado no local especificado será executado totalmente confiável.</span><span class="sxs-lookup"><span data-stu-id="d842b-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d842b-130">Um modelo de formulário é carregado a partir do computador local (grupo de código de zona do meu computador) seja carregado pelo InfoPath usando uma URL aleatória.</span><span class="sxs-lookup"><span data-stu-id="d842b-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="d842b-131">Por esse motivo, você não pode usar o procedimento a seguir para conceder a permissão FullTrust definida como tal um modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="d842b-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="d842b-132">Para conceder a permissão FullTrust de um modelo de formulário instalado localmente definida, use um dos procedimentos descritos na seção "Implantando o formulário modelos que exigem confiança total" do tópico [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="d842b-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="d842b-133">Para atribuir FullTrust para formulários do InfoPath em um local específico de URL ou UNC</span><span class="sxs-lookup"><span data-stu-id="d842b-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="d842b-134">No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="d842b-135">Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="d842b-136">Em **Meu computador**, expanda o nó de **Diretiva de segurança de tempo de execução** , o nó de **máquina** , o nó de **Grupos de código** , o nó **All_Code** e, em seguida, clique no nó de **Modelos de formulário do InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="d842b-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="d842b-137">Na lista de **tarefas** no painel direito, clique em **Adicionar um grupo de códigos filho**, o nome do grupo de código e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d842b-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="d842b-138">Na lista **Escolher o tipo de condição para este grupo de código** , selecione a **URL**e, em seguida, insira a URL ou UNC para a localização dos modelos de formulário de código gerenciado do InfoPath que você deseja conceder **a permissão FullTrust** .</span><span class="sxs-lookup"><span data-stu-id="d842b-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="d842b-139">Para restringir a permissão definida como um modelo de formulário simples, especifique o caminho completo do modelo de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="d842b-139">To restrict the permission set to a single form template, specify the full path of that particular form template.</span></span> <span data-ttu-id="d842b-140">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d842b-140">For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `http://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="d842b-141">Para conceder a permissão definida como todos os modelos de formulário em uma URL ou UNC, omita o nome do modelo e adicione um asterisco no final da URL ou UNC.</span><span class="sxs-lookup"><span data-stu-id="d842b-141">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC.</span></span> <span data-ttu-id="d842b-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d842b-142">For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `http://MySite/MySubsite/*`
    
5. <span data-ttu-id="d842b-143">Clique em **Avançar**, **conjunto de permissões de uso existente** e clique atribua a permissão **FullTrust** definida como código de grupo.</span><span class="sxs-lookup"><span data-stu-id="d842b-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="d842b-144">Clique em **Avançar**e, em seguida, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="d842b-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="d842b-145">Para aplicar as novas configurações, feche e reinicie o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d842b-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d842b-146">Para aplicar um conjunto de permissões mais restritivas ou personalizado, selecione a opção apropriada em vez de **FullTrust** na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="d842b-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="d842b-147">Criando um pacote de implantação para a diretiva de segurança do InfoPath</span><span class="sxs-lookup"><span data-stu-id="d842b-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="d842b-148">Depois de definir a diretiva de segurança personalizada para modelos de formulário gerenciado do InfoPath, você pode criar um pacote do Windows Installer (. msi) para implantar essa diretiva de segurança nos computadores dos usuários usando a diretiva de grupo ou o Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="d842b-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="d842b-149">Para criar um pacote de implantação para a diretiva de segurança personalizada do InfoPath</span><span class="sxs-lookup"><span data-stu-id="d842b-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="d842b-150">No menu **Iniciar** , aponte para **Ferramentas administrativas**e clique em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="d842b-151">Se você não tiver **Ferramentas administrativas** no menu **Iniciar** , no **Painel de controle** de abrir **Ferramentas administrativas**e, em seguida, clique duas vezes em **configuração do Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d842b-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="d842b-152">Com o botão direito **Em tempo de execução de diretiva de segurança**e, em seguida, clique em **Criar pacote de implantação**.</span><span class="sxs-lookup"><span data-stu-id="d842b-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="d842b-153">Em **Selecione a política de segurança para implantar**, clique em **automática**, especifique a pasta e o nome do arquivo de pacote do Windows Installer e, em seguida, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="d842b-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="d842b-154">Clique em **Concluir** para criar o pacote de implantação.</span><span class="sxs-lookup"><span data-stu-id="d842b-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="d842b-155">Para obter informações sobre como usar a ferramenta de configuração do .NET Framework, pesquise a Ajuda do Visual Studio ou o site do MSDN "Ferramenta .NET Framework Configuration (Mscorcfg. msc)".</span><span class="sxs-lookup"><span data-stu-id="d842b-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN Web site for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d842b-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="d842b-156">See also</span></span>



[<span data-ttu-id="d842b-157">Sobre o modelo de segurança para modelos de formulário com código</span><span class="sxs-lookup"><span data-stu-id="d842b-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

