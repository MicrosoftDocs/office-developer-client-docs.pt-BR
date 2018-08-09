---
title: Testar recursos, autenticação e configuração
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 69e1f5bc-354c-4c33-84a1-b1aa10d4b650
description: Este tópico descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.
ms.openlocfilehash: ac294291e2226dbb73f822b2a641fe2bf67ce5eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770956"
---
# <a name="testing-capabilities-authentication-and-configuration"></a><span data-ttu-id="2af53-103">Testar recursos, autenticação e configuração</span><span class="sxs-lookup"><span data-stu-id="2af53-103">Testing capabilities, authentication, and configuration</span></span>

<span data-ttu-id="2af53-104">Este tópico descreve os testes para obtenção de recursos e cenários em torno Configurando uma conta e autenticação de um usuário para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="2af53-104">This topic describes tests for getting capabilities, and scenarios around configuring an account and authenticating a user for a social network.</span></span>
  
## <a name="getting-capabilities"></a><span data-ttu-id="2af53-105">Recursos de Introdução</span><span class="sxs-lookup"><span data-stu-id="2af53-105">Getting capabilities</span></span>

<span data-ttu-id="2af53-106">Um provedor do Outlook Social Connector (OSC) implementa [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)e as chamadas OSC **GetCapabilities** para obter a funcionalidade suportada pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="2af53-106">A Outlook Social Connector (OSC) provider implements [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), and the OSC calls **GetCapabilities** to get the functionality supported by the provider.</span></span> <span data-ttu-id="2af53-107">Os recursos que o provedor oferece suporte para a sua rede social devem ser conhecidos no ponto de implementação e não devem depender de uma chamada para a rede social em tempo real.</span><span class="sxs-lookup"><span data-stu-id="2af53-107">The capabilities that your provider supports for your social network should be known at the point of implementation, and should not depend on a call to the social network in real time.</span></span> <span data-ttu-id="2af53-108">Por exemplo, os usuários do Outlook podem iniciar o Outlook offline e **GetCapabilities** não pode depender da conectividade de rede no momento quando o Outlook for iniciado.</span><span class="sxs-lookup"><span data-stu-id="2af53-108">For example, Outlook users can start Outlook offline, and **GetCapabilities** cannot rely on network connectivity at the time when Outlook starts.</span></span> 
  
<span data-ttu-id="2af53-109">Ao testar o provedor, você deve verificar se o parâmetro de sequência de _resultados_ retornado pelo **GetCapabilities** está em conformidade com o elemento de **recursos** conforme definido pelo esquema XML de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="2af53-109">When testing the provider, you should verify that the  _results_ string parameter returned by **GetCapabilities** conforms to the **capabilities** element as defined by the OSC provider XML schema.</span></span> <span data-ttu-id="2af53-110">Para obter mais informações, consulte [Elementos XML de recursos](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="2af53-110">For more information, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span>
  
## <a name="configuring-an-account"></a><span data-ttu-id="2af53-111">Configurando uma conta</span><span class="sxs-lookup"><span data-stu-id="2af53-111">Configuring an account</span></span>

<span data-ttu-id="2af53-112">Quando o OSC configura uma conta, você deve verificar se o ícone de redes sociais e o nome são exibidas e se os hiperlinks criar conta e senha esqueceu são exibidas na caixa de diálogo de configuração de conta, conforme especificado pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="2af53-112">When the OSC configures an account, you should verify whether the social network icon and name are displayed, and that the create-account and forgot-password hyperlinks appear in the account configuration dialog box as specified by the provider.</span></span>
  
### <a name="social-network-icon-and-name"></a><span data-ttu-id="2af53-113">Nome e o ícone de redes sociais</span><span class="sxs-lookup"><span data-stu-id="2af53-113">Social network icon and name</span></span>

<span data-ttu-id="2af53-114">Depois de obter recursos, o OSC poderá continuar a fazer o ícone e o nome para a rede social chamando [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) e [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md).</span><span class="sxs-lookup"><span data-stu-id="2af53-114">After getting capabilities, the OSC can proceed to get the icon and name for the social network by calling [ISocialProvider::SocialNetworkIcon](isocialprovider-socialnetworkicon.md) and [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md).</span></span> <span data-ttu-id="2af53-115">Execute os seguintes testes para verificar que essas chamadas de método bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2af53-115">Do the following tests to verify that these method calls succeed.</span></span>
  
|<span data-ttu-id="2af53-116">**Item de teste**</span><span class="sxs-lookup"><span data-stu-id="2af53-116">**Item to test**</span></span>|<span data-ttu-id="2af53-117">**Comportamento esperado**</span><span class="sxs-lookup"><span data-stu-id="2af53-117">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2af53-118">Ícone de redes sociais</span><span class="sxs-lookup"><span data-stu-id="2af53-118">Social network icon</span></span>  <br/> | <span data-ttu-id="2af53-119">O ícone de rede social é exibido corretamente nos seguintes locais no OSC:</span><span class="sxs-lookup"><span data-stu-id="2af53-119">The social network icon is displayed correctly in the following places in the OSC:</span></span>  <br/>  <span data-ttu-id="2af53-120">Na caixa de diálogo OSC para **Contas de rede Social**.</span><span class="sxs-lookup"><span data-stu-id="2af53-120">In the OSC dialog box for **Social Network Accounts**.</span></span>  <br/>  <span data-ttu-id="2af53-121">No menu suspenso quando você tentar adicionar uma pessoa como um amigo.</span><span class="sxs-lookup"><span data-stu-id="2af53-121">In the drop-down menu when you attempt to add a person as a friend.</span></span>  <br/>  <span data-ttu-id="2af53-122">No crachá quando seguindo um amigo.</span><span class="sxs-lookup"><span data-stu-id="2af53-122">In the badge when following a friend.</span></span>  <br/> <br/><span data-ttu-id="2af53-123">**Observação**: você pode acessar a caixa de diálogo para **Contas de rede Social** clicando na guia **Exibir** , no Outlook, no **Painel pessoas** grupo, clicando em **Painel de pessoas**e, em seguida, clicando em **Configurações de conta**.</span><span class="sxs-lookup"><span data-stu-id="2af53-123">**NOTE**:  You can access the dialog box for **Social Network Accounts** by clicking the **View** tab in Outlook, in the **People Pane** group, clicking **People Pane**, and then clicking **Account Settings**.</span></span>           |
|<span data-ttu-id="2af53-124">Nome de rede social</span><span class="sxs-lookup"><span data-stu-id="2af53-124">Social network name</span></span>  <br/> | <span data-ttu-id="2af53-125">O nome de rede social é exibido corretamente nos seguintes locais no OSC:</span><span class="sxs-lookup"><span data-stu-id="2af53-125">The social network name is displayed correctly in the following places in the OSC:</span></span>  <br/>  <span data-ttu-id="2af53-126">Na caixa de diálogo OSC para **Contas de rede Social**.</span><span class="sxs-lookup"><span data-stu-id="2af53-126">In the OSC dialog box for **Social Network Accounts**.</span></span>  <br/>  <span data-ttu-id="2af53-127">No menu suspenso quando você tentar adicionar uma pessoa como um amigo.</span><span class="sxs-lookup"><span data-stu-id="2af53-127">In the drop-down menu when you attempt to add a person as a friend.</span></span>  <br/>  <span data-ttu-id="2af53-128">Como o título da caixa de diálogo senha quando você tentar alterar a senha existente.</span><span class="sxs-lookup"><span data-stu-id="2af53-128">As the title of the password dialog box when you attempt to change the existing password.</span></span>  <br/> |
   
### <a name="showing-hyperlinks-in-configuration-dialog"></a><span data-ttu-id="2af53-129">Mostrando hiperlinks na caixa de diálogo de configuração</span><span class="sxs-lookup"><span data-stu-id="2af53-129">Showing hyperlinks in configuration dialog</span></span>

<span data-ttu-id="2af53-130">Depois de chamar **ISocialProvider::GetCapabilities**, o OSC usa o valor do elemento **hideHyperlinks** no parâmetro _resultados_ para determinar se deseja ocultar ou exibir o **clique aqui para criar uma conta** e **Esqueceu sua senha?** hiperlinks na caixa de diálogo de configuração de conta.</span><span class="sxs-lookup"><span data-stu-id="2af53-130">After calling **ISocialProvider::GetCapabilities**, the OSC uses the value of the **hideHyperlinks** element in the  _results_ parameter to determine whether to hide or display the **Click here to create an account** and **Forgot your password?** hyperlinks in the account configuration dialog box.</span></span> <span data-ttu-id="2af53-131">Verifique se se **hideHyperlinks** for **false**, a configuração da conta exibe essas URLs.</span><span class="sxs-lookup"><span data-stu-id="2af53-131">Verify that if **hideHyperlinks** is **false**, the account configuration displays these URLs.</span></span>
  
### <a name="support-to-create-account"></a><span data-ttu-id="2af53-132">Suporte para criar conta</span><span class="sxs-lookup"><span data-stu-id="2af53-132">Support to create account</span></span>

<span data-ttu-id="2af53-133">Verifique se o parâmetro de _resultados_ na chamada de método **ISocialProvider::GetCapabilities** tem o elemento **hideHyperlinks** definida como **false** e o elemento **createAccountUrl** definido como **true**, clicando na URL Abre a página no navegador da web padrão.</span><span class="sxs-lookup"><span data-stu-id="2af53-133">Verify that if the  _results_ parameter from the **ISocialProvider::GetCapabilities** method call has the **hideHyperlinks** element set to **false** and the **createAccountUrl** element set to **true**, clicking the URL opens the page in the default web browser.</span></span>
  
### <a name="support-for-forgotten-password"></a><span data-ttu-id="2af53-134">Suporte para recuperação de senha</span><span class="sxs-lookup"><span data-stu-id="2af53-134">Support for forgotten password</span></span>

<span data-ttu-id="2af53-135">Verifique se o parâmetro de _resultados_ na chamada de método **ISocialProvider::GetCapabilities** tem o elemento **hideHyperlinks** definida como **false** e o elemento **forgotPasswordUrl** definido como **true**, clicando na URL Abre a página no navegador da web padrão.</span><span class="sxs-lookup"><span data-stu-id="2af53-135">Verify that if the  _results_ parameter from the **ISocialProvider::GetCapabilities** method call has the **hideHyperlinks** element set to **false** and the **forgotPasswordUrl** element set to **true**, clicking the URL opens the page in the default web browser.</span></span>
  
## <a name="authenticating-users"></a><span data-ttu-id="2af53-136">Autenticação de usuários</span><span class="sxs-lookup"><span data-stu-id="2af53-136">Authenticating users</span></span>

<span data-ttu-id="2af53-137">Teste para os seguintes cenários independentemente se o seu provedor OSC oferece suporte à autenticação básica ou autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="2af53-137">Test for the following scenarios regardless of whether your OSC provider supports basic authentication or forms-based authentication.</span></span>
  
|<span data-ttu-id="2af53-138">**Cenário**</span><span class="sxs-lookup"><span data-stu-id="2af53-138">**Scenario**</span></span>|<span data-ttu-id="2af53-139">**Comportamento esperado**</span><span class="sxs-lookup"><span data-stu-id="2af53-139">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2af53-140">Fazendo logon pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="2af53-140">Logging on for the first time.</span></span>  <br/> |<span data-ttu-id="2af53-141">O usuário pode fazer logon com êxito à rede social.</span><span class="sxs-lookup"><span data-stu-id="2af53-141">The user can successfully log on to the social network.</span></span>  <br/> |
|<span data-ttu-id="2af53-142">Logon com uma senha formada por uma variedade de caracteres, incluindo pontuação e caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="2af53-142">Logging on with a password made up of a variety of characters, including punctuation and Unicode characters.</span></span>  <br/> |<span data-ttu-id="2af53-143">O usuário pode fazer logon com êxito à rede social, independente do tipo de caracteres usados na senha.</span><span class="sxs-lookup"><span data-stu-id="2af53-143">The user can successfully log on to the social network, independent of the kind of characters used in the password.</span></span>  <br/> |
|<span data-ttu-id="2af53-144">A caixa de diálogo **Contas de rede Social** exibindo o nome de usuário ou a ID.</span><span class="sxs-lookup"><span data-stu-id="2af53-144">The dialog box for **Social Network Accounts** displaying the user name or ID.</span></span>  <br/> |<span data-ttu-id="2af53-145">Depois que o usuário tem com êxito conectado à rede, a caixa de diálogo do OSC para **Contas de rede Social** exibe o nome do usuário conectado ou o ID.</span><span class="sxs-lookup"><span data-stu-id="2af53-145">After the user has successfully logged on to the network, the OSC's dialog box for **Social Network Accounts** displays the logged-on user name or ID.</span></span>  <br/> |
|<span data-ttu-id="2af53-146">A autenticação falhará.</span><span class="sxs-lookup"><span data-stu-id="2af53-146">Authentication fails.</span></span>  <br/> |<span data-ttu-id="2af53-147">O OSC exibe o erro de **nome de usuário inválido ou a senha**.</span><span class="sxs-lookup"><span data-stu-id="2af53-147">The OSC displays the error **Invalid user name or password**.</span></span>  <br/> |
|<span data-ttu-id="2af53-148">Não é possível conectar-se à rede social.</span><span class="sxs-lookup"><span data-stu-id="2af53-148">Cannot connect to the social network.</span></span>  <br/> |<span data-ttu-id="2af53-149">O OSC exibe o erro no **servidor não pode ser encontrado**.</span><span class="sxs-lookup"><span data-stu-id="2af53-149">The OSC displays the error **Server cannot be found**.</span></span>  <br/> |
|<span data-ttu-id="2af53-150">Ser capaz de recuperar itens.</span><span class="sxs-lookup"><span data-stu-id="2af53-150">Being able to retrieve items.</span></span>  <br/> |<span data-ttu-id="2af53-151">Depois que o usuário autenticado, todas as atividades devem ser permitidas.</span><span class="sxs-lookup"><span data-stu-id="2af53-151">Once the user has authenticated, all activity should be allowed.</span></span> <span data-ttu-id="2af53-152">Não há nenhum erro Obtendo dados ou atividades de amigos dos.</span><span class="sxs-lookup"><span data-stu-id="2af53-152">There are no errors getting friends' data or activities.</span></span>  <br/> |
|<span data-ttu-id="2af53-153">Fazer logon na rede de social após a reinicialização do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2af53-153">Logging on to the social network after restarting Outlook.</span></span>  <br/> |<span data-ttu-id="2af53-154">Se o provedor do OSC permitir o armazenamento em cache da senha, depois que o usuário autenticado na primeira vez, o usuário não é subsequentemente solicitado credenciais sempre que o OSC tenta obter dados a partir da rede social.</span><span class="sxs-lookup"><span data-stu-id="2af53-154">If the OSC provider allows caching of the password, after the user has authenticated the first time, the user is not subsequently prompted for credentials whenever the OSC attempts to get data from the social network.</span></span>  <br/> |
   
<span data-ttu-id="2af53-155">Além disso, se seu provedor OSC suporta a autenticação baseada em formulários, teste para o seguinte cenário.</span><span class="sxs-lookup"><span data-stu-id="2af53-155">In addition, if your OSC provider supports forms-based authentication, test for the following scenario as well.</span></span>
  
|<span data-ttu-id="2af53-156">**Cenário**</span><span class="sxs-lookup"><span data-stu-id="2af53-156">**Scenario**</span></span>|<span data-ttu-id="2af53-157">**Comportamento esperado**</span><span class="sxs-lookup"><span data-stu-id="2af53-157">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2af53-158">O OSC obtendo uma URL para um formulário para o usuário fazer logon de chamar [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).</span><span class="sxs-lookup"><span data-stu-id="2af53-158">The OSC getting a URL to a form for the user to log on from calling [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md).</span></span>  <br/> |<span data-ttu-id="2af53-159">O OSC abre a URL no navegador de padrão do usuário e a página da Web permite que o usuário insira credenciais para fazer logon na rede social.</span><span class="sxs-lookup"><span data-stu-id="2af53-159">The OSC opens the URL in the user's default browser, and the webpage allows the user to enter credentials to log on to the social network.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2af53-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="2af53-160">See also</span></span>

- [<span data-ttu-id="2af53-161">Elementos XML de recursos</span><span class="sxs-lookup"><span data-stu-id="2af53-161">Capabilities XML Elements</span></span>](capabilities-xml-elements.md)  
- [<span data-ttu-id="2af53-162">Autenticação básica</span><span class="sxs-lookup"><span data-stu-id="2af53-162">Basic Authentication</span></span>](basic-authentication.md) 
- [<span data-ttu-id="2af53-163">Autenticação baseada em formulários</span><span class="sxs-lookup"><span data-stu-id="2af53-163">Forms-Based Authentication</span></span>](forms-based-authentication.md)
- [<span data-ttu-id="2af53-164">Preparando-se para o lançamento de um provedor OSC</span><span class="sxs-lookup"><span data-stu-id="2af53-164">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
