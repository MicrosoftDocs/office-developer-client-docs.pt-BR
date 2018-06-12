---
title: Integração de aplicativos de mensagens Instantâneas com o Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artigo descreve como configurar um aplicativo de cliente de mensagem instantânea (IM), para que ele se integra os recursos sociais no Office 2013, incluindo exibindo a presença e enviar mensagens instantâneas do cartão de visita.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771191"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="80d38-103">Integração de aplicativos de mensagens Instantâneas com o Office</span><span class="sxs-lookup"><span data-stu-id="80d38-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="80d38-104">Este artigo descreve como configurar um aplicativo de cliente de mensagem instantânea (IM), para que ele se integra os recursos sociais no Office 2013, incluindo exibindo a presença e enviar mensagens instantâneas do cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="80d38-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="80d38-105">Se você tiver quaisquer dúvidas ou comentários sobre este artigo técnico ou os processos que ele descreve, contate a Microsoft diretamente enviando um email para [docthis@microsoft.com](mailto:docthis@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="80d38-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="80d38-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="80d38-106">Introduction</span></span>
<span data-ttu-id="80d38-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-107"></span></span>

<span data-ttu-id="80d38-108">Office 2013 fornece integração rica com o cliente de mensagens Instantâneas de aplicativos, incluindo o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="80d38-108">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="80d38-109">Essa integração oferece aos usuários recursos de mensagens Instantâneas de dentro do Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 e OneNote 2013, bem como oferecendo integração de presença em páginas do SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="80d38-109">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="80d38-110">Os usuários podem ver as fotos, o nome, o status de presença e entre em contato com dados de pessoas em sua lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="80d38-110">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="80d38-111">Elas podem começar uma sessão de mensagens Instantâneas, chamada de vídeo ou chamada telefônica diretamente do cartão de visita (o elemento de interface do usuário no Office 2013 que mostra as opções de comunicação e informações de contato).</span><span class="sxs-lookup"><span data-stu-id="80d38-111">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="80d38-112">Office 2013 facilita ficar conectado aos seus contatos sem levá-lo fora do seu email ou documentos.</span><span class="sxs-lookup"><span data-stu-id="80d38-112">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80d38-113">Este artigo usa o termo aplicativo cliente de mensagens Instantâneas para referir-se especificamente para o aplicativo instalado no computador de um usuário que se comunica com o serviço de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-113">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="80d38-114">Por exemplo, Lync 2013 é considerado um aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-114">For example, Lync 2013 is considered an IM client application.</span></span> <span data-ttu-id="80d38-115">Este artigo não fornece detalhes sobre como o aplicativo cliente de mensagens Instantâneas comunica-se ao serviço de mensagens Instantâneas ou sobre o próprio serviço de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-115">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="80d38-116">Você pode personalizar um aplicativo de cliente de mensagens Instantâneas para que ele se comunica com o Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-116">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="80d38-117">Especificamente, você pode modificar o seu aplicativo de mensagens Instantâneas para que exiba as seguintes informações na interface do usuário do Office:</span><span class="sxs-lookup"><span data-stu-id="80d38-117">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="80d38-118">Fotos do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-118">Contact photo.</span></span>
    
- <span data-ttu-id="80d38-119">Nome do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-119">Contact name.</span></span>
    
- <span data-ttu-id="80d38-120">Entre em contato com a nota de status pessoal.</span><span class="sxs-lookup"><span data-stu-id="80d38-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="80d38-121">Entre em contato com o status de presença.</span><span class="sxs-lookup"><span data-stu-id="80d38-121">Contact presence status.</span></span>
    
- <span data-ttu-id="80d38-122">Entre em contato com a cadeia de caracteres de disponibilidade (por exemplo, "Disponível" ou "ausência temporária").</span><span class="sxs-lookup"><span data-stu-id="80d38-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="80d38-123">Entre em contato com a cadeia de caracteres de recurso (por exemplo, "vídeo pronto").</span><span class="sxs-lookup"><span data-stu-id="80d38-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="80d38-124">Lançamento de mensagens Instantâneas de um clique.</span><span class="sxs-lookup"><span data-stu-id="80d38-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="80d38-125">Início da chamada de vídeo de um clique.</span><span class="sxs-lookup"><span data-stu-id="80d38-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="80d38-126">Início da chamada telefônica com um clique (incluindo SIP, número de telefone, caixa postal e novo número de chamada).</span><span class="sxs-lookup"><span data-stu-id="80d38-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="80d38-127">Gerenciamento de contatos (Adicionar ao grupo de mensagens Instantâneas).</span><span class="sxs-lookup"><span data-stu-id="80d38-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="80d38-128">Entre em contato com o local e fuso horário.</span><span class="sxs-lookup"><span data-stu-id="80d38-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="80d38-129">Dados de contato, número de telefone, endereço de email, título e nome da empresa.</span><span class="sxs-lookup"><span data-stu-id="80d38-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="80d38-130">**Figura 1. Cartão de visita no Office 2013**</span><span class="sxs-lookup"><span data-stu-id="80d38-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="80d38-131">![O cartão de pessoas no Office 2013] (media/ocom15_peoplecard.png "O cartão de pessoas no Office 2013")</span><span class="sxs-lookup"><span data-stu-id="80d38-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="80d38-132">Para habilitar essa integração com o Office, um aplicativo de cliente de mensagens Instantâneas deve implementar um conjunto de interfaces que o Office oferece para se conectar a ela.</span><span class="sxs-lookup"><span data-stu-id="80d38-132">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="80d38-133">As APIs para essa integração estão incluídas no namespace [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que está contido no arquivo dll, que é instalado com as versões do Office 2013 que incluem Lync / Skype para negócios.</span><span class="sxs-lookup"><span data-stu-id="80d38-133">The APIs for this integration are included in the [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="80d38-134">O namespace **UCCollaborationLib** inclui as interfaces que você deve implementar para integração com o Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-134">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="80d38-135">Biblioteca de tipos para as interfaces necessárias está incorporada no Lync 2013/Skype para negócios.</span><span class="sxs-lookup"><span data-stu-id="80d38-135">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="80d38-136">Para integradores de terceiros, isso funciona apenas quando o Lync 2013 e Skype para negócios estão instalados no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="80d38-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="80d38-137">Se você estiver integrando usando Office Standard, você precisará extrair a biblioteca de tipos e instalá-lo no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="80d38-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="80d38-138">O [SDK do Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) inclui o arquivo dll.</span><span class="sxs-lookup"><span data-stu-id="80d38-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="80d38-139">Um número limitado de aplicativos do Office 2010 pode integrar da mesma forma, com um aplicativo de provedor IM de terceiros: Outlook 2010, o Word 2010, o Excel 2010, o PowerPoint 2010 e o SharePoint Server 2010 (usando um controle ActiveX).</span><span class="sxs-lookup"><span data-stu-id="80d38-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="80d38-140">Muitas das etapas necessárias para integração com o Office 2013 se aplicam também para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="80d38-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="80d38-141">Há várias das principais diferenças em como o Office 2010 é integrado com um aplicativo do provedor de mensagens Instantâneas:</span><span class="sxs-lookup"><span data-stu-id="80d38-141">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="80d38-142">Office 2010 não exibe fotos do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-142">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="80d38-143">Você deve baixar o arquivo DLL separadamente do Office 2010.</span><span class="sxs-lookup"><span data-stu-id="80d38-143">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="80d38-144">O [SDK do Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) inclui o arquivo DLL para o Office 2010.</span><span class="sxs-lookup"><span data-stu-id="80d38-144">The [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="80d38-145">Quando o aplicativo Office chama o método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) no aplicativo do cliente de mensagens Instantâneas, ele passa na cadeia de caracteres "14.0.0.0".</span><span class="sxs-lookup"><span data-stu-id="80d38-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="80d38-146">Office 2010 enumera todos os grupos e contatos assim que ele se conecta a um aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-146">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="80d38-147">Como o Office é integrado com um aplicativo de cliente de mensagens Instantâneas</span><span class="sxs-lookup"><span data-stu-id="80d38-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="80d38-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-148"></span></span>

<span data-ttu-id="80d38-149">Quando um aplicativo do Office 2013 for iniciado, ele vai através do seguinte processo para integrar com o aplicativo de cliente de mensagens Instantâneas padrão:</span><span class="sxs-lookup"><span data-stu-id="80d38-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="80d38-150">Ele verifica o registro para descobrir o aplicativo de cliente de mensagens Instantâneas padrão e, em seguida, conecta-se a ela.</span><span class="sxs-lookup"><span data-stu-id="80d38-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="80d38-151">Ele autentica com o aplicativo cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="80d38-152">Ele se conecta ao interfaces específicas que são expostos pelo aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="80d38-153">Ele determina os recursos do usuário conectado (usuário local), incluindo a obtenção de contatos do usuário, determinando a presença do usuário e determinar os recursos de IM do usuário (mensagens instantâneas, conversa com vídeo, VOIP e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="80d38-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="80d38-154">Ela obtém informações de presença de contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="80d38-155">Quando o aplicativo cliente de mensagens Instantâneas desligado, o aplicativo do Office 2013 se desconecta silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="80d38-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="80d38-156">Descobrir o aplicativo de mensagens Instantâneas</span><span class="sxs-lookup"><span data-stu-id="80d38-156">Discovering the IM application</span></span>

<span data-ttu-id="80d38-157">O aplicativo Office procura por vários teclas específicas e entradas no registro para descobrir o aplicativo de cliente de mensagens Instantâneas padrão.</span><span class="sxs-lookup"><span data-stu-id="80d38-157">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="80d38-158">Se descobrir a um aplicativo de cliente de mensagens Instantâneas padrão e, em seguida, ele tenta se conectar a ela.</span><span class="sxs-lookup"><span data-stu-id="80d38-158">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="80d38-159">O processo que o aplicativo Office passa para descobrir o aplicativo de cliente de mensagens Instantâneas padrão é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="80d38-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="80d38-160">O aplicativo Office procura para ver se a subchave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp no registro é definida e lê o nome do aplicativo na lista.</span><span class="sxs-lookup"><span data-stu-id="80d38-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="80d38-161">Em seguida, o aplicativo Office lê a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_e monitora o valor para que as alterações.</span><span class="sxs-lookup"><span data-stu-id="80d38-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="80d38-162">Em seguida, o aplicativo Office lê a chave de registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _nome do aplicativo_ e obtém os valores de ID (CLSID) Nome_do_processo e a classe armazenados nela.</span><span class="sxs-lookup"><span data-stu-id="80d38-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="80d38-163">Depois que o aplicativo cliente de mensagens Instantâneas tiver concluído sua sequência iniciar com êxito e registrados todas as classes corretamente para a integração de presença, ele define a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_para "2" indicando que o aplicativo de cliente está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="80d38-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="80d38-164">Quando o aplicativo Office descobre que a chave de \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _nome do aplicativo_tiver sido definida como "2", ele verificará a lista de processos em execução no computador para que o nome do processo do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="80d38-165">Depois que o aplicativo Office localiza o processo que usa o aplicativo de cliente de mensagens Instantâneas, o aplicativo Office chama **CoCreateInstance** usando o CLSID para estabelecer uma conexão para o aplicativo cliente de mensagens Instantâneas como um servidor de COM fora do processo.</span><span class="sxs-lookup"><span data-stu-id="80d38-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="80d38-166">Autenticar a conexão para o aplicativo de mensagens Instantâneas</span><span class="sxs-lookup"><span data-stu-id="80d38-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="80d38-167">Depois que o aplicativo Office estabelece uma conexão para o aplicativo cliente de mensagens Instantâneas, em seguida, acontece o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80d38-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="80d38-168">O aplicativo Office chama o método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) para verificar se há a interface [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) .</span><span class="sxs-lookup"><span data-stu-id="80d38-168">The Office application calls [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="80d38-169">O aplicativo do Office, em seguida, chama o método **IUCOfficeIntegration.GetAuthenticationInfo** , passando a versão mais recente a integração com suporte (por exemplo, "15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="80d38-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="80d38-170">Se o aplicativo cliente de mensagens Instantâneas suporta a versão do Office passado como um parâmetro, o aplicativo retorna a seguinte sequência XML codificadas ao código de chamada:</span><span class="sxs-lookup"><span data-stu-id="80d38-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="80d38-171">Por motivos de herança, o aplicativo cliente de mensagens Instantâneas deve retornar o valor exato `<authenticationinfo>` para a chamada para **GetAuthenticationInfo** se ele oferece suporte a versão do Office passado como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="80d38-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="80d38-172">Se o aplicativo cliente de mensagens Instantâneas não retorna um valor, o aplicativo Office chama o método **GetAuthenticationInfo** novamente com a próxima versão com suporte mais alto do Office (por exemplo, "14.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="80d38-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="80d38-173">Depois que o Office determina que o aplicativo cliente de mensagens Instantâneas oferece suporte a integração de mensagens Instantâneas e presença, ele se conecta a um conjunto necessário das interfaces termine a inicialização.</span><span class="sxs-lookup"><span data-stu-id="80d38-173">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="80d38-174">(Para obter mais informações, consulte [Connecting to interfaces necessárias](#off15_IMIntegration_HowConnect).)</span><span class="sxs-lookup"><span data-stu-id="80d38-174">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="80d38-175">Se o aplicativo Office encontra um erro em qualquer uma das etapas acima, ele faz o check-out e integração de presença não é estabelecida novamente durante a sessão do aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="80d38-176">Conectando-se a interfaces necessárias</span><span class="sxs-lookup"><span data-stu-id="80d38-176">Connecting to required interfaces</span></span>
<span data-ttu-id="80d38-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-177"></span></span>

<span data-ttu-id="80d38-178">Depois de autenticar a conexão para o aplicativo cliente de mensagens Instantâneas, o aplicativo do Office tenta se conectar a um conjunto de interfaces necessárias que o aplicativo cliente de mensagens Instantâneas deve expor.</span><span class="sxs-lookup"><span data-stu-id="80d38-178">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="80d38-179">O aplicativo Office realiza isso fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80d38-179">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="80d38-180">O aplicativo Office obtém um objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) chamando o método **IUCOfficeIntegration.GetInterface** , passando o **oiInterfaceLyncClient** constante da enumeração [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) .</span><span class="sxs-lookup"><span data-stu-id="80d38-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="80d38-181">O aplicativo Office obtém um objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) chamando o método **IUCOfficeIntegration.GetInterface** , passando o **oiInterfaceAutomation** constante da enumeração **OIInterface** .</span><span class="sxs-lookup"><span data-stu-id="80d38-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="80d38-182">O aplicativo Office configura o ouvinte de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) .</span><span class="sxs-lookup"><span data-stu-id="80d38-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="80d38-183">O aplicativo Office configura o ouvinte de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) .</span><span class="sxs-lookup"><span data-stu-id="80d38-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="80d38-184">O aplicativo Office obtém o estado de entrada do aplicativo de cliente de mensagens Instantâneas, acessando a propriedade **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="80d38-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="80d38-185">O aplicativo Office obtém os recursos do aplicativo cliente IM chamando o método **IUCOfficeIntegration.GetSupportedFeatures** , que retorna um sinalizador provenientes da enumeração [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="80d38-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="80d38-186">O aplicativo Office acessa a propriedade **ILyncClient.Self** para obter uma referência a um objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="80d38-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="80d38-187">Recuperando os recursos do usuário local</span><span class="sxs-lookup"><span data-stu-id="80d38-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="80d38-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-188"></span></span>

<span data-ttu-id="80d38-189">O aplicativo Office obtém os recursos do usuário local, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80d38-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="80d38-190">Se o aplicativo cliente de mensagens Instantâneas dá suporte à interface **IClient2** , Office tentará obter um objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) acessando a propriedade **IClient2.PrivateContactManager** .</span><span class="sxs-lookup"><span data-stu-id="80d38-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="80d38-191">Se o aplicativo de mensagens Instantâneas não oferece suporte para a interface **IClient2** , o aplicativo Office obtém um objeto de **IContactManager** acessando a propriedade **ILyncClient.ContactManager** .</span><span class="sxs-lookup"><span data-stu-id="80d38-191">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="80d38-192">O aplicativo cliente de mensagens Instantâneas com êxito deve retornar um objeto **IContactManager** antes que quaisquer outros recursos de mensagem Instantânea podem ser estabelecidos.</span><span class="sxs-lookup"><span data-stu-id="80d38-192">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="80d38-193">O aplicativo Office acessa a propriedade **ILyncClient.Uri** e, em seguida, chama **IContactManager.GetContactByUri** para obter o objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) associado ao usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="80d38-194">O aplicativo do Office, em seguida, faz várias chamadas para **IContact.CanStart** para estabelecer as capacidades do usuário local, passando os valores para **ModalityTypes.ucModalityInstantMessage** e **ModalityTypes.ucModalityAudioVideo** sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="80d38-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="80d38-195">Recuperando a presença de contato</span><span class="sxs-lookup"><span data-stu-id="80d38-195">Retrieving contact presence</span></span>
<span data-ttu-id="80d38-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-196"></span></span>

<span data-ttu-id="80d38-197">O aplicativo Office obtém a presença de contato, incluindo o usuário local, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80d38-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="80d38-198">O aplicativo Office chama **IContact.GetContactInformation** para obter um item de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="80d38-199">Em seguida, o aplicativo do Office se inscreve para alteração de status de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-199">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="80d38-200">Ela chama **IContactManager.CreateSubscription** para obter um objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="80d38-200">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="80d38-201">Ela chama **IContactSubscription.AddContact** para adicionar o contato à assinatura de e, em seguida, chama **IContactSubscription.Subscribe** para fazer alterações no status do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-201">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="80d38-202">Se o aplicativo de mensagens Instantâneas suporta **IContact2**, Office tenta obter informações de presença chamando **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="80d38-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="80d38-203">O aplicativo do Office, em seguida, recupera as propriedades de presença do contato chamando **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="80d38-203">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="80d38-204">O aplicativo do Office pode obter um segundo conjunto de propriedades de presença, acessando a propriedade **IContact.Settings** .</span><span class="sxs-lookup"><span data-stu-id="80d38-204">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="80d38-205">Finalmente, o aplicativo Office obtém a associação de grupo do contato acessando a propriedade **IContact.CustomGroups** .</span><span class="sxs-lookup"><span data-stu-id="80d38-205">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="80d38-206">Isso retorna uma coleção de [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que inclui todos os objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que o contato pertencer a.</span><span class="sxs-lookup"><span data-stu-id="80d38-206">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="80d38-207">Desconectar-se de que o aplicativo de mensagens Instantâneas</span><span class="sxs-lookup"><span data-stu-id="80d38-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="80d38-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-208"></span></span>

<span data-ttu-id="80d38-209">Quando o aplicativo do Office 2013 detecta o evento **OnShuttingDown** do aplicativo de mensagens Instantâneas, ele desconecta silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="80d38-209">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="80d38-210">No entanto, se o aplicativo Office desligado antes que o aplicativo de mensagens Instantâneas, o aplicativo do Office não garante que a conexão é limpos.</span><span class="sxs-lookup"><span data-stu-id="80d38-210">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="80d38-211">O aplicativo de mensagens Instantâneas deve tratar vazamento de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="80d38-211">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="80d38-212">Entradas e chaves de registro de configuração</span><span class="sxs-lookup"><span data-stu-id="80d38-212">Setting registry keys and entries</span></span>
<span data-ttu-id="80d38-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-213"></span></span>

<span data-ttu-id="80d38-214">Conforme mencionado anteriormente, os aplicativos do Office com capacidade para mensagens Instantâneas 2013 procuram teclas específicas, entradas e valores do registro para descobrir o aplicativo cliente de mensagens Instantâneas para se conectar ao.</span><span class="sxs-lookup"><span data-stu-id="80d38-214">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="80d38-215">Esses valores do registro fornecem o aplicativo do Office com o nome de processo e o CLSID da classe que atua como o ponto de partida para o modelo de objeto do aplicativo de cliente de mensagens Instantâneas (ou seja, a classe que implementa a interface **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="80d38-215">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="80d38-216">O aplicativo Office co cria essa classe e conecta-se como um cliente no servidor fora do processo COM o aplicativo cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-216">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="80d38-217">Use a tabela 1 para identificar as chaves, entradas e valores que precisam ser gravados no registro para integrar um aplicativo de cliente de mensagens Instantâneas com o Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="80d38-218">**Tabela 1. Chaves do registro para configurar o aplicativo de cliente de mensagens Instantâneas padrão**</span><span class="sxs-lookup"><span data-stu-id="80d38-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="80d38-219">**Key**</span><span class="sxs-lookup"><span data-stu-id="80d38-219">**Key**</span></span>|<span data-ttu-id="80d38-220">**Entry**</span><span class="sxs-lookup"><span data-stu-id="80d38-220">**Entry**</span></span>|<span data-ttu-id="80d38-221">**Tipo de**</span><span class="sxs-lookup"><span data-stu-id="80d38-221">**Type**</span></span>|<span data-ttu-id="80d38-222">**Valor**</span><span class="sxs-lookup"><span data-stu-id="80d38-222">**Value**</span></span>|<span data-ttu-id="80d38-223">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="80d38-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="80d38-224">Provedores de HKEY_LOCAL_MACHINE\Software\IM\\< nome do aplicativo\></span><span class="sxs-lookup"><span data-stu-id="80d38-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="80d38-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="80d38-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="80d38-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="80d38-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="80d38-227">O nome do aplicativo de cliente IM de terceiros.</span><span class="sxs-lookup"><span data-stu-id="80d38-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="80d38-228">Litware IM 2012</span><span class="sxs-lookup"><span data-stu-id="80d38-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="80d38-229">Nome_do_processo</span><span class="sxs-lookup"><span data-stu-id="80d38-229">ProcessName</span></span>  <br/> |<span data-ttu-id="80d38-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="80d38-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="80d38-231">O nome do processo do aplicativo de cliente IM de terceiros.</span><span class="sxs-lookup"><span data-stu-id="80d38-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="80d38-232">Litware.exe</span><span class="sxs-lookup"><span data-stu-id="80d38-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="80d38-233">GUID</span><span class="sxs-lookup"><span data-stu-id="80d38-233">GUID</span></span>  <br/> |<span data-ttu-id="80d38-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="80d38-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="80d38-235">Uma ID da classe (CLSID) para a raiz, a classe cocreatable no aplicativo de mensagens Instantâneas (a classe que implementa a interface **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="80d38-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="80d38-236">(UMA GUID)</span><span class="sxs-lookup"><span data-stu-id="80d38-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="80d38-237">Provedores de HKEY_CURRENT_USER\Software\IM</span><span class="sxs-lookup"><span data-stu-id="80d38-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="80d38-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="80d38-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="80d38-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="80d38-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="80d38-240">O nome do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-240">The name of the IM client application.</span></span> <span data-ttu-id="80d38-241">Isso deve ser o mesmo que o nome da chave do registro de nível superior (hive) na HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="80d38-241">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="80d38-242">Litware</span><span class="sxs-lookup"><span data-stu-id="80d38-242">Litware</span></span>  <br/> |
|<span data-ttu-id="80d38-243">Provedores de HKEY_CURRENT_USER\Software\IM\\< nome do aplicativo\></span><span class="sxs-lookup"><span data-stu-id="80d38-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="80d38-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="80d38-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="80d38-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="80d38-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="80d38-246">Um valor inteiro entre 0 e 2:</span><span class="sxs-lookup"><span data-stu-id="80d38-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="80d38-247">0 — não funcionando</span><span class="sxs-lookup"><span data-stu-id="80d38-247">0—Not running</span></span>  <br/>  <span data-ttu-id="80d38-248">1 — Iniciando</span><span class="sxs-lookup"><span data-stu-id="80d38-248">1—Starting</span></span>  <br/>  <span data-ttu-id="80d38-249">2 — executando</span><span class="sxs-lookup"><span data-stu-id="80d38-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="80d38-250">**Observação**: A chave de registro de nome do aplicativo deve ser o mesmo que o valor da entrada DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="80d38-250">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="80d38-251">Implementando as interfaces necessárias para integração com o Office</span><span class="sxs-lookup"><span data-stu-id="80d38-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="80d38-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-252"></span></span>

<span data-ttu-id="80d38-253">Existem três interfaces do namespace **UCCollaborationLib** executável (ou servidor COM) de um aplicativo de cliente de mensagens Instantâneas deve implementar para que ele pode se integrar com o Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-253">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="80d38-254">Se essas interfaces não são implementadas, o aplicativo Office faz o check-out durante o processo de inicialização e a conexão com o aplicativo cliente de mensagens Instantâneas não é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="80d38-254">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="80d38-255">As interfaces necessárias são:</span><span class="sxs-lookup"><span data-stu-id="80d38-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="80d38-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)— Embora não seja obrigatório, a interface **_IUCOfficeIntegrationEvents** também deve ser implementada na mesma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="80d38-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="80d38-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)— Embora não seja obrigatório, a interface **_ILyncClientEvents** também deve ser implementada na mesma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="80d38-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="80d38-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="80d38-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="80d38-259">Interface de IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="80d38-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="80d38-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-260"></span></span>

<span data-ttu-id="80d38-261">A interface de **IUCOfficeIntegration** fornece o ponto de entrada para um aplicativo do Office para se conectar ao aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-261">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="80d38-262">A interface define três métodos que chama um aplicativo do Office como parte do processo de iniciar uma conexão com o aplicativo cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-262">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="80d38-263">A classe que implementa a interface **IUCOfficeIntegration** deve ser co creatable para que o Office co pode criar uma instância dele.</span><span class="sxs-lookup"><span data-stu-id="80d38-263">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="80d38-264">Além disso, ele deve expor o CLSID que é inserido como o valor para a entrada GUID na chave do registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _nome do aplicativo_ .</span><span class="sxs-lookup"><span data-stu-id="80d38-264">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="80d38-265">A classe que herda de **IUCOfficeIntegration** também deve implementar a interface **_IUCOfficeIntegrationEvents** .</span><span class="sxs-lookup"><span data-stu-id="80d38-265">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="80d38-266">A interface de **_IUCOfficeIntegrationEvents** contém os membros que exponham os manipuladores de eventos da interface **IUCOfficeIntegration** .</span><span class="sxs-lookup"><span data-stu-id="80d38-266">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="80d38-267">Tabela 2 mostra os membros que devem ser implementados na classe que herda de **IUCOfficeIntegration** e **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="80d38-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-268">Para obter mais informações sobre o **IUCOfficeIntegration** e interfaces **_IUCOfficeIntegrationEvents** e seus membros, consulte [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) e [UCCollaborationLib._IUCOfficeIntegrationEvents ](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="80d38-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="80d38-269">**Tabela 2. Implementação das interfaces IUCOfficeIntegration e _IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="80d38-270">**Interface**</span><span class="sxs-lookup"><span data-stu-id="80d38-270">**Interface**</span></span>|<span data-ttu-id="80d38-271">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-271">**Member**</span></span>|<span data-ttu-id="80d38-272">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d38-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="80d38-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="80d38-274">Método **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="80d38-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="80d38-275">Obtém a sequência de informações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="80d38-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="80d38-276">Método **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="80d38-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="80d38-277">Obtém a interface de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="80d38-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="80d38-278">Método **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="80d38-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="80d38-279">Obtém os recursos de integração do Office com suporte.</span><span class="sxs-lookup"><span data-stu-id="80d38-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="80d38-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="80d38-281">Evento **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="80d38-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="80d38-282">O evento acionado quando o aplicativo cliente de mensagens Instantâneas está tentando desligar.</span><span class="sxs-lookup"><span data-stu-id="80d38-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="80d38-283">Use o código a seguir para definir uma classe que os herda as interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegration** dentro de um aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="80d38-284">O método de **GetAuthenticationInfo** aceita uma cadeia de caracteres como um argumento para o parâmetro de _versão_ .</span><span class="sxs-lookup"><span data-stu-id="80d38-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="80d38-285">Quando o aplicativo Office chama esse método, ele passa de uma das duas cadeias de caracteres para o argumento, dependendo da versão do Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="80d38-286">Quando o aplicativo Office fornece o método com a versão do Office que suporta o aplicativo cliente de mensagens Instantâneas (ou seja, suporta a funcionalidade), o método **GetAuthenticationInfo** retorna uma cadeia de caracteres XML codificadas `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="80d38-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="80d38-287">Use o código a seguir para implementar o método **GetAuthentication** dentro do código de aplicativo do cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="80d38-288">O método **GetInterface** coloca referências às classes ao código de chamada, dependendo de qual é passado como um argumento para o parâmetro de _interface_ .</span><span class="sxs-lookup"><span data-stu-id="80d38-288">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="80d38-289">Quando um aplicativo do Office chama o método **GetInterface** , passa em um dos dois valores para o parâmetro interface: a constante **oiInterfaceILyncClient** (1) ou a constante **oiInterfaceIAutomation** (2) do [ UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeração.</span><span class="sxs-lookup"><span data-stu-id="80d38-289">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="80d38-290">Se o aplicativo Office passa na constante **oiInterfaceILyncClient** , o método **GetInterface** retorna uma referência a uma classe que implementa a interface **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="80d38-290">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="80d38-291">Se o aplicativo Office passa na constante **oiInterfaceIAutomation** , o método **GetInterface** retorna uma classe que implementa a interface **IAutomation** .</span><span class="sxs-lookup"><span data-stu-id="80d38-291">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="80d38-292">Use o exemplo de código a seguir para implementar o método **GetInterface** dentro do código de aplicativo do cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="80d38-293">O método **GetSupportedFeatures** retorna informações sobre os recursos de mensagens Instantâneas que suporta o aplicativo cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-293">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="80d38-294">Leva uma cadeia de caracteres para seu único parâmetro, a _versão_.</span><span class="sxs-lookup"><span data-stu-id="80d38-294">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="80d38-295">Quando o aplicativo Office chama o método **GetSupportFeatures** , o método retorna um valor da enumeração [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="80d38-295">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="80d38-296">O valor retornado especifica os recursos do cliente de mensagens Instantâneas, onde cada recurso do aplicativo de cliente de mensagens Instantâneas é indicado para o aplicativo do Office, adicionando um sinalizador com o valor.</span><span class="sxs-lookup"><span data-stu-id="80d38-296">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="80d38-297">Aplicativos do Office 2013 ignoram as seguintes constantes na enumeração **OIFeature** :</span><span class="sxs-lookup"><span data-stu-id="80d38-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="80d38-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="80d38-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="80d38-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="80d38-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="80d38-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="80d38-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="80d38-301">Use o exemplo de código a seguir para implementar o método **GetSupportFeatures** dentro do código de aplicativo do cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="80d38-302">Interface de ILyncClient</span><span class="sxs-lookup"><span data-stu-id="80d38-302">ILyncClient interface</span></span>
<span data-ttu-id="80d38-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-303"></span></span>

<span data-ttu-id="80d38-304">A interface **ILyncClient** mapeia para os recursos do aplicativo de cliente de mensagens Instantâneas em si.</span><span class="sxs-lookup"><span data-stu-id="80d38-304">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="80d38-305">Ele expõe as propriedades que se referem a pessoa que está conectada ao aplicativo (o usuário local, representado pela interface [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), o estado do aplicativo, a lista de contatos, a para o usuário local e várias outras configurações.</span><span class="sxs-lookup"><span data-stu-id="80d38-305">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="80d38-306">Quando ele tenta se conectar ao aplicativo de cliente de mensagens Instantâneas, o aplicativo Office obtém uma referência a um objeto que implementa a interface **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="80d38-306">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="80d38-307">Essa referência, Office pode acessar grande parte da funcionalidade do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-307">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="80d38-308">Além disso, a classe que implementa a interface **ILyncClient** também deve implementar a interface **_ILyncClientEvents** .</span><span class="sxs-lookup"><span data-stu-id="80d38-308">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="80d38-309">A interface **_ILyncClientEvents** expõe vários eventos que são necessários para o monitoramento do estado do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-309">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="80d38-310">A tabela 3 mostra os membros que devem ser implementados na classe que herda de **ILyncClient** e **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="80d38-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-311">Qualquer membro do **ILyncClient** ou ** \_ILyncClientEvents** interface não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-311">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-312">Membros que estão presentes, mas não implementado podem acionar uma **NotImplementedException** ou **f\_NOTIMPL** erro.</span><span class="sxs-lookup"><span data-stu-id="80d38-312">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="80d38-313">Para obter mais informações sobre o **ILyncClient** e interfaces **_ILyncClientEvents** e seus membros, consulte [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) e [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="80d38-313">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="80d38-314">**Tabela 3. Implementação das interfaces ILyncClient e ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="80d38-315">**Interface**</span><span class="sxs-lookup"><span data-stu-id="80d38-315">**Interface**</span></span>|<span data-ttu-id="80d38-316">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-316">**Member**</span></span>|<span data-ttu-id="80d38-317">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d38-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="80d38-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="80d38-319">Propriedade **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="80d38-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="80d38-320">Obtém o gerente de grupo de contatos.</span><span class="sxs-lookup"><span data-stu-id="80d38-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="80d38-321">Propriedade **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="80d38-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="80d38-322">Obtém o Gerenciador de conversas.</span><span class="sxs-lookup"><span data-stu-id="80d38-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="80d38-323">Propriedade **Self**</span><span class="sxs-lookup"><span data-stu-id="80d38-323">**Self** property</span></span>  <br/> |<span data-ttu-id="80d38-324">Obtém o objeto **Self** .</span><span class="sxs-lookup"><span data-stu-id="80d38-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="80d38-325">Método de **logon**</span><span class="sxs-lookup"><span data-stu-id="80d38-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="80d38-326">Inicia o aplicativo de cliente de mensagens Instantâneas entrar processo com uma disponibilidade específica.</span><span class="sxs-lookup"><span data-stu-id="80d38-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="80d38-327">Propriedade **State**</span><span class="sxs-lookup"><span data-stu-id="80d38-327">**State** property</span></span>  <br/> |<span data-ttu-id="80d38-328">Obtém o estado atual da plataforma.</span><span class="sxs-lookup"><span data-stu-id="80d38-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="80d38-329">Propriedade **URI**</span><span class="sxs-lookup"><span data-stu-id="80d38-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="80d38-330">Obtém o URI do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="80d38-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="80d38-332">Evento **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="80d38-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="80d38-333">Gerado quando o estado de aplicativo do cliente de mensagens Instantâneas é alterado.</span><span class="sxs-lookup"><span data-stu-id="80d38-333">Raised when the IM client application state changes.</span></span> <span data-ttu-id="80d38-334">Você deve lidar com esse evento e obter a propriedade **eventData.NewState** .</span><span class="sxs-lookup"><span data-stu-id="80d38-334">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="80d38-335">O evento é disparado para todos os processos vinculados a uma instância de um aplicativo de cliente de mensagens Instantâneas quando qualquer subsistema no aplicativo faz com que a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="80d38-335">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="80d38-336">Durante o processo de inicialização, Office acessa a propriedade **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="80d38-336">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="80d38-337">Esta propriedade deve retornar um valor da enumeração [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) .</span><span class="sxs-lookup"><span data-stu-id="80d38-337">This property needs to return a value from the [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="80d38-338">A propriedade **State** armazena o status atual do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-338">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="80d38-339">Deve ser definido e atualizado em toda a sessão de aplicativo do cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-339">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="80d38-340">Quando a mensagem Instantânea aplicativo cliente entra no, desconecta-se ou desligado, ele deve definir a propriedade **State** .</span><span class="sxs-lookup"><span data-stu-id="80d38-340">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="80d38-341">É melhor definir essa propriedade dentro os métodos **ILyncClient.SignIn** e **ILyncClient.SignOut** , como o exemplo a seguir demonstra.</span><span class="sxs-lookup"><span data-stu-id="80d38-341">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="80d38-342">O exemplo de código a seguir demonstra como configurar o ouvinte de eventos usando o _ **ILyncClientEvents** e _ **IUCOfficeIntegrationEvents** interfaces.</span><span class="sxs-lookup"><span data-stu-id="80d38-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="80d38-343">Interface de IAutomation</span><span class="sxs-lookup"><span data-stu-id="80d38-343">IAutomation interface</span></span>
<span data-ttu-id="80d38-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-344"></span></span>

<span data-ttu-id="80d38-345">A interface **IAutomation** automatiza recursos do aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-345">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="80d38-346">Ele pode ser usado para iniciar conversas, ingressar em conferências e fornecer um contexto de janela de extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="80d38-346">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="80d38-347">A tabela 4 mostra os membros que devem ser implementados na classe que herda de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="80d38-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-348">Qualquer membro da interface **IAutomation** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-349">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="80d38-350">Para obter mais informações sobre a interface **IAutomation** e seus membros, consulte [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="80d38-350">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="80d38-351">**Tabela 4. Implementação da interface IAutomation**</span><span class="sxs-lookup"><span data-stu-id="80d38-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="80d38-352">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-352">**Member**</span></span>|<span data-ttu-id="80d38-353">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-354">Método **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="80d38-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="80d38-355">Inicia uma conversa usando a modalidade de conversa especificado.</span><span class="sxs-lookup"><span data-stu-id="80d38-355">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="80d38-356">Uma instância de **IConversationWindow** é retornada.</span><span class="sxs-lookup"><span data-stu-id="80d38-356">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="80d38-357">Implementando a integração de presença do contato</span><span class="sxs-lookup"><span data-stu-id="80d38-357">Implementing contact presence integration</span></span>
<span data-ttu-id="80d38-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-358"></span></span>

<span data-ttu-id="80d38-359">Além das interfaces obrigatórias três discutidas anteriormente, existem várias outras interfaces que são importantes para habilitar a funcionalidade de presença de contato no Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-359">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="80d38-360">Isso inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80d38-360">These include the following:</span></span>
  
- <span data-ttu-id="80d38-361">A interface [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) ou **IContact2** .</span><span class="sxs-lookup"><span data-stu-id="80d38-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="80d38-362">A interface [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="80d38-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="80d38-363">As interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) e [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) .</span><span class="sxs-lookup"><span data-stu-id="80d38-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="80d38-364">As interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) e [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) .</span><span class="sxs-lookup"><span data-stu-id="80d38-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="80d38-365">A interface [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="80d38-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="80d38-366">A interface [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) .</span><span class="sxs-lookup"><span data-stu-id="80d38-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="80d38-367">A interface [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="80d38-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="80d38-368">Interface de IContact</span><span class="sxs-lookup"><span data-stu-id="80d38-368">IContact interface</span></span>
<span data-ttu-id="80d38-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-369"></span></span>

<span data-ttu-id="80d38-370">A interface **IContact** representa um usuário de aplicativo do cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-370">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="80d38-371">A interface expõe a presença, pelas modalidades disponíveis, a associação ao grupo e as propriedades de tipo de contato para um usuário.</span><span class="sxs-lookup"><span data-stu-id="80d38-371">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="80d38-372">Para iniciar uma conversa com outro usuário, você deve fornecer essa instância do usuário do **IContact**.</span><span class="sxs-lookup"><span data-stu-id="80d38-372">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="80d38-373">Tabela 5 mostra os membros que devem ser implementados na classe que herda de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="80d38-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-374">Qualquer membro da interface **IContact** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-375">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="80d38-376">Para obter mais informações sobre a interface **IContact** e seus membros, consulte [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="80d38-376">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="80d38-377">**Tabela 5. Implementação da interface IContact**</span><span class="sxs-lookup"><span data-stu-id="80d38-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="80d38-378">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-378">**Member**</span></span>|<span data-ttu-id="80d38-379">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-380">Método **CanStart**</span><span class="sxs-lookup"><span data-stu-id="80d38-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="80d38-381">Retorna **true** se um determinado tipo de modalidade pode ser iniciado no contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="80d38-382">Método **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="80d38-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="80d38-383">Obtém um item de presença de um contato de publicação.</span><span class="sxs-lookup"><span data-stu-id="80d38-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="80d38-384">Método **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="80d38-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="80d38-385">Obtém a vários itens de presença de um contato de publicação.</span><span class="sxs-lookup"><span data-stu-id="80d38-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="80d38-386">Propriedade **Settings**</span><span class="sxs-lookup"><span data-stu-id="80d38-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="80d38-387">Obtém uma coleção de propriedades do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="80d38-388">Propriedade **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="80d38-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="80d38-389">Obtém uma coleção dos grupos que o contato é um membro de.</span><span class="sxs-lookup"><span data-stu-id="80d38-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="80d38-390">Durante o processo de inicialização, o aplicativo Office chama o método **IContact.CanStart** para determinar os recursos de mensagens Instantâneas para o usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-390">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="80d38-391">O método **CanStart** leva um sinalizador provenientes da enumeração [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como um argumento para o parâmetro de_modalityTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="80d38-391">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter.</span></span> <span data-ttu-id="80d38-392">Se o usuário atual pode participar a modalidade solicitada (ou seja, o usuário é capaz de mensagens instantâneas, áudio e vídeo de mensagens ou compartilhamento de aplicativos), o método **CanStart** retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="80d38-392">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="80d38-393">O método **GetContactInformation** recupera informações sobre o contato do objeto **IContact** .</span><span class="sxs-lookup"><span data-stu-id="80d38-393">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="80d38-394">O código de chamada precisa passar um valor da enumeração [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para o parâmetro_contactInformationType_ _, que indica os dados a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="80d38-394">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="80d38-395">Assim como o **GetContactInformation**, o método **BatchGetContactInformation** recupera vários itens de presença sobre o contato do objeto **IContact** .</span><span class="sxs-lookup"><span data-stu-id="80d38-395">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="80d38-396">O código de chamada precisa passar uma matriz de valores da enumeração **ContactInformationType** para o parâmetro de_contactInformationTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="80d38-396">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter.</span></span> <span data-ttu-id="80d38-397">O método retorna um objeto de [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contém os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="80d38-397">The method returns an [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="80d38-398">A propriedade **IContact.Settings** retorna um objeto de **IContactSettingDictionary** que contém as propriedades personalizadas sobre o contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="80d38-399">A propriedade **IContact.CustomGroups** retorna um objeto **IGroupCollection** que inclui todos os grupos dos quais o contato é membro.</span><span class="sxs-lookup"><span data-stu-id="80d38-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="80d38-400">Interface de ISelf</span><span class="sxs-lookup"><span data-stu-id="80d38-400">ISelf interface</span></span>
<span data-ttu-id="80d38-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-401"></span></span>

<span data-ttu-id="80d38-402">Durante o processo de inicialização, o aplicativo Office obtém os dados para o usuário atual, acessando a propriedade **ILyncClient.Self** , que deve retornar um objeto **ISelf** .</span><span class="sxs-lookup"><span data-stu-id="80d38-402">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="80d38-403">A interface **ISelf** representa o usuário de aplicativo de cliente de mensagens Instantâneas de local, conectado.</span><span class="sxs-lookup"><span data-stu-id="80d38-403">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="80d38-404">Tabela 6 mostra os membros que devem ser implementados na classe que herda de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="80d38-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-405">Qualquer membro da interface **ISelf** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-405">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-406">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-406">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="80d38-407">**Tabela 6. Implementação da interface ISelf**</span><span class="sxs-lookup"><span data-stu-id="80d38-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="80d38-408">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-408">**Member**</span></span>|<span data-ttu-id="80d38-409">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-410">Propriedade **Contact**</span><span class="sxs-lookup"><span data-stu-id="80d38-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="80d38-411">Obtém o objeto **IContact** associado ao usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="80d38-412">Presença, pelas modalidades disponíveis, a associação ao grupo e as propriedades de tipo de contato para o usuário local são expostas por meio da propriedade **ISelf.Contact** (que retorna um objeto **IContact** ).</span><span class="sxs-lookup"><span data-stu-id="80d38-412">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="80d38-413">Durante o processo de inicialização, o aplicativo Office acessa a propriedade **ISelf.Contact** para obter uma referência para as informações de contato para o usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-413">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="80d38-414">Use o código a seguir para definir uma classe que herda da interface **ISelf** que implementa a propriedade do **contato** .</span><span class="sxs-lookup"><span data-stu-id="80d38-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="80d38-415">Interfaces IContactManager e _IContactManagerEvents</span><span class="sxs-lookup"><span data-stu-id="80d38-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="80d38-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-416"></span></span>

<span data-ttu-id="80d38-417">O objeto **IContactManager** gerencia os contatos do usuário local, incluindo as informações de contato do local do próprio usuário.</span><span class="sxs-lookup"><span data-stu-id="80d38-417">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="80d38-418">O aplicativo Office usa um objeto **IContactManager** para acessar objetos de **IContact** que correspondem aos contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-418">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="80d38-419">A tabela 7 mostra os membros que devem ser implementados na classe que herda de **IContactManager** e **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="80d38-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-420">Qualquer membro da interface **IContactManager** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-421">Membros que estão presentes, mas não implementado podem acionar uma **NotImplementedException** ou **f\_NOTIMPL** erro.</span><span class="sxs-lookup"><span data-stu-id="80d38-421">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="80d38-422">Para obter mais informações sobre o **IContactManager** e interfaces **_IContactManagerEvents** e seus membros, consulte [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) e [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="80d38-422">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="80d38-423">**A tabela 7. Implementação das interfaces IContactManager e _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="80d38-424">**Interface**</span><span class="sxs-lookup"><span data-stu-id="80d38-424">**Interface**</span></span>|<span data-ttu-id="80d38-425">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-425">**Member**</span></span>|<span data-ttu-id="80d38-426">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d38-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="80d38-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="80d38-428">Método **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="80d38-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="80d38-429">Localiza ou cria uma nova instância de contato usando o URI do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="80d38-430">Método **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="80d38-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="80d38-431">Cria um objeto **ISubscription** que pode ser usado para processamento em lotes assinaturas ou consultas.</span><span class="sxs-lookup"><span data-stu-id="80d38-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="80d38-432">Método **proc**</span><span class="sxs-lookup"><span data-stu-id="80d38-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="80d38-433">Pesquise um contato ou grupo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="80d38-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="80d38-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="80d38-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="80d38-435">Evento **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="80d38-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="80d38-436">Acionado quando um grupo é adicionado a uma coleção de grupo.</span><span class="sxs-lookup"><span data-stu-id="80d38-436">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="80d38-437">A coleção de grupo atualizados pode ser obtida da propriedade **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="80d38-437">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="80d38-438">Evento **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="80d38-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="80d38-439">Acionado quando um grupo é removido de uma coleção de grupo.</span><span class="sxs-lookup"><span data-stu-id="80d38-439">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="80d38-440">A coleção de grupo atualizados pode ser obtida da propriedade **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="80d38-440">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="80d38-441">Evento **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="80d38-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="80d38-442">Acionado quando o status do provedor de pesquisa for alterado.</span><span class="sxs-lookup"><span data-stu-id="80d38-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="80d38-443">O Office chama **IContactManager.GetContactByUri** para obter informações de presença de um contato, usando o endereço SIP do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-443">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="80d38-444">Quando um contato estiver configurado para um endereço SIP no Active Directory, o Office determina esse endereço para um contato e chamadas **GetContactByUri**, passando o endereço SIP do contato no parâmetro __contactUri_ .</span><span class="sxs-lookup"><span data-stu-id="80d38-444">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="80d38-445">Quando o Office não puder determinar o endereço SIP do contato, ele chama o método **IContactManager.Lookup** para localizar o SIP usando o serviço de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-445">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="80d38-446">Aqui Office passa nos dados recomendados que ele possa encontrar para o contato (por exemplo, apenas o endereço de email do contato).</span><span class="sxs-lookup"><span data-stu-id="80d38-446">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="80d38-447">O método **Lookup** assincronamente retorna um objeto **AsynchronousOperation** .</span><span class="sxs-lookup"><span data-stu-id="80d38-447">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="80d38-448">Quando invoca o retorno de chamada, o método de **pesquisa** deve retornar o êxito ou falha da operação além o URI do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-448">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="80d38-449">O aplicativo do Office precisa se inscrever para alterações de presença para um contato individual.</span><span class="sxs-lookup"><span data-stu-id="80d38-449">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="80d38-450">Assim, quando o status de presença do contato for alterado, o servidor de mensagens Instantâneas avisa o aplicativo cliente de mensagens Instantâneas — alertas, portanto, o aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="80d38-450">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="80d38-451">Para fazer isso, o aplicativo Office chama o método **IContactManager.CreateSubscription** para criar um novo objeto de **IContactSubscription** para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="80d38-451">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="80d38-452">Interfaces IGroup e IGroupCollection</span><span class="sxs-lookup"><span data-stu-id="80d38-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="80d38-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-453"></span></span>

<span data-ttu-id="80d38-454">O objeto **IGroup** representa uma coleção de contatos com propriedades adicionais para identificar o conjunto de contatos por nome de um grupo coletivo.</span><span class="sxs-lookup"><span data-stu-id="80d38-454">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="80d38-455">Um objeto **IGroupCollection** representa uma coleção de objetos **IGroup** definido por um usuário local e o aplicativo de cliente de mensagens Instantâneas.</span><span class="sxs-lookup"><span data-stu-id="80d38-455">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="80d38-456">O aplicativo do Office usa os objetos **IGroupCollection** e **IGroup** para acessar os contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="80d38-456">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="80d38-457">A tabela 9 mostra os membros que devem ser implementados nas classes que herdam **IGroup** e **IGroupCollection** na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80d38-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80d38-458">Qualquer membro da interface **IGroup** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-459">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="80d38-460">Para obter mais informações sobre as interfaces **IGroup** e **IGroupCollection** e seus membros, consulte [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) e [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="80d38-460">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="80d38-461">**A tabela 9. Implementação das interfaces IGroup e IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="80d38-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="80d38-462">**Interface**</span><span class="sxs-lookup"><span data-stu-id="80d38-462">**Interface**</span></span>|<span data-ttu-id="80d38-463">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-463">**Member**</span></span>|<span data-ttu-id="80d38-464">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d38-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="80d38-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="80d38-466">Propriedade **Count**</span><span class="sxs-lookup"><span data-stu-id="80d38-466">**Count** property</span></span>  <br/> |<span data-ttu-id="80d38-467">Retorna a contagem de objetos **IGroup** na coleção</span><span class="sxs-lookup"><span data-stu-id="80d38-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="80d38-468">Propriedade **item**</span><span class="sxs-lookup"><span data-stu-id="80d38-468">**Item** property</span></span>  <br/> |<span data-ttu-id="80d38-469">Retorna o objeto **IGroup** no índice especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="80d38-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="80d38-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="80d38-470">**IGroup**</span></span> <br/> |<span data-ttu-id="80d38-471">Propriedade **ID**</span><span class="sxs-lookup"><span data-stu-id="80d38-471">**Id** property</span></span>  <br/> |<span data-ttu-id="80d38-472">Retorna a identificação do grupo.</span><span class="sxs-lookup"><span data-stu-id="80d38-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="80d38-473">Quando o aplicativo Office obtém as informações do usuário local, ele acessa as associações de grupo do contato (usuário local) chamando-se a propriedade **IContact.CustomGroups** , que retorna um objeto **IGroupCollection** .</span><span class="sxs-lookup"><span data-stu-id="80d38-473">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="80d38-474">O **IGroupCollection** deve conter uma matriz (ou **lista**) de objetos **IGroup** .</span><span class="sxs-lookup"><span data-stu-id="80d38-474">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="80d38-475">A classe derivada de **IGroupCollection** deve expor uma propriedade **Count** , que retorna o número de itens na coleção e um método de indexador, **this(int)**, que retorna um objeto **IGroup** da coleção.</span><span class="sxs-lookup"><span data-stu-id="80d38-475">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="80d38-476">Interface de IContactSubscription</span><span class="sxs-lookup"><span data-stu-id="80d38-476">IContactSubscription interface</span></span>
<span data-ttu-id="80d38-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-477"></span></span>

<span data-ttu-id="80d38-478">A interface **IContactSubscription** permite que você especifique os contatos para receber notificações e atualizações de informações de presença para os tipos de informações de presença que acionam uma notificação.</span><span class="sxs-lookup"><span data-stu-id="80d38-478">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="80d38-479">Aplicativos do Office usam um objeto **IContactSubscription** para registrar as alterações para o status de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-479">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="80d38-480">A tabela 10 mostra os membros que devem ser implementados nas classes que herdam **IContactSubscription**.</span><span class="sxs-lookup"><span data-stu-id="80d38-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-481">Qualquer membro da interface **IContactSubscription** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-482">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="80d38-483">Para obter mais informações sobre a interface **IContactSubscription** e seus membros, consulte [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="80d38-483">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="80d38-484">**Tabela 10. Implementação da interface IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="80d38-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="80d38-485">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-485">**Member**</span></span>|<span data-ttu-id="80d38-486">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-487">Método **AddContact**</span><span class="sxs-lookup"><span data-stu-id="80d38-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="80d38-488">Adiciona um contato para o objeto de inscrição.</span><span class="sxs-lookup"><span data-stu-id="80d38-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="80d38-489">Método **Subscribe**</span><span class="sxs-lookup"><span data-stu-id="80d38-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="80d38-490">Ajuda o aplicativo cliente de mensagens Instantâneas para monitorar a presença de um contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="80d38-491">A interface **IContactSubscription** deve conter uma referência a todos os objetos **IContact** monitora, usando uma matriz ou uma **lista**.</span><span class="sxs-lookup"><span data-stu-id="80d38-491">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="80d38-492">O método **IContactSubscription.AddContact** adiciona um objeto **IContact** para na estrutura de dados subjacente do objeto **IContactSubscription** , assim, adicionando um novo contato para o monitoramento de alterações de presença.</span><span class="sxs-lookup"><span data-stu-id="80d38-492">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="80d38-493">O método **IContactSubscription.Subscribe** permite que um aplicativo cliente de mensagens Instantâneas acessar observadores de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-493">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="80d38-494">Ele pode usar uma estratégia de sondagem para obter que as informações de presença do servidor para os contatos para que o aplicativo cliente de mensagens Instantâneas assinou.</span><span class="sxs-lookup"><span data-stu-id="80d38-494">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="80d38-495">O método **Subscribe** é útil em situações onde a presença é solicitada para alguém de fora da lista de contatos do usuário (por exemplo, a partir de uma rede pública maior).</span><span class="sxs-lookup"><span data-stu-id="80d38-495">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="80d38-496">Interface de IContactEndPoint</span><span class="sxs-lookup"><span data-stu-id="80d38-496">IContactEndPoint interface</span></span>
<span data-ttu-id="80d38-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-497"></span></span>

<span data-ttu-id="80d38-498">O **IContactEndPoint** representa um número de telefone da coleção de um contato de números de telefone.</span><span class="sxs-lookup"><span data-stu-id="80d38-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="80d38-499">A tabela 11 mostra os membros que devem ser implementados nas classes que herdam **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="80d38-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-500">Qualquer membro da interface **IContactEndPoint** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-501">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="80d38-502">Para obter mais informações sobre a interface **IContactEndPoint** e seus membros, consulte [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="80d38-502">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="80d38-503">**A tabela 11. Implementação da interface IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="80d38-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="80d38-504">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-504">**Member**</span></span>|<span data-ttu-id="80d38-505">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-506">Propriedade **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="80d38-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="80d38-507">Obtém a cadeia de caracteres de exibição.</span><span class="sxs-lookup"><span data-stu-id="80d38-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="80d38-508">Propriedade **Type**</span><span class="sxs-lookup"><span data-stu-id="80d38-508">**Type** property</span></span>  <br/> |<span data-ttu-id="80d38-509">Obtém o tipo de contato do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="80d38-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="80d38-510">Propriedade **URI**</span><span class="sxs-lookup"><span data-stu-id="80d38-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="80d38-511">Obtém o URI do contato.</span><span class="sxs-lookup"><span data-stu-id="80d38-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="80d38-512">Interface de ILocaleString</span><span class="sxs-lookup"><span data-stu-id="80d38-512">ILocaleString interface</span></span>
<span data-ttu-id="80d38-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="80d38-513"></span></span>

<span data-ttu-id="80d38-514">O **ILocaleString** é uma estrutura de cadeia de caracteres localizada que contém uma cadeia de caracteres localizada e a identificação de localidade da localização.</span><span class="sxs-lookup"><span data-stu-id="80d38-514">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="80d38-515">A interface de **ILocaleString** é utilizada para formatar a cadeia de caracteres de status personalizados no cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="80d38-515">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="80d38-516">12 de tabela mostra os membros que devem ser implementados nas classes que herdam **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="80d38-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80d38-517">Qualquer membro da interface **ILocaleString** não listado na tabela deve estar presente, mas não precisará ser implementado.</span><span class="sxs-lookup"><span data-stu-id="80d38-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="80d38-518">Membros que estão presentes, mas não implementado podem acionar um erro **NotImplementedException** ou **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="80d38-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="80d38-519">Para obter mais informações sobre a interface **ILocalString** e seus membros, consulte [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="80d38-519">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="80d38-520">**A tabela 12. Implementação da interface ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="80d38-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="80d38-521">**Membro**</span><span class="sxs-lookup"><span data-stu-id="80d38-521">**Member**</span></span>|<span data-ttu-id="80d38-522">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="80d38-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d38-523">Propriedade **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="80d38-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="80d38-524">Obtém a ID de localidade.</span><span class="sxs-lookup"><span data-stu-id="80d38-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="80d38-525">Propriedade **Value**</span><span class="sxs-lookup"><span data-stu-id="80d38-525">**Value** property</span></span>  <br/> |<span data-ttu-id="80d38-526">Obtém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="80d38-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80d38-527">Confira também</span><span class="sxs-lookup"><span data-stu-id="80d38-527">See also</span></span>

- <span data-ttu-id="80d38-528">Namespace [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="80d38-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

