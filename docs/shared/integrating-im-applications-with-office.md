---
title: Integração de aplicativos de mensagens instantâneas ao Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: Este artigo descreve como configurar um aplicativo cliente de mensagens instantâneas para que ele se integre aos recursos de redes sociais no Office 2013, incluindo exibir presença e enviar mensagens instantâneas do cartão de visita.
localization_priority: Priority
ms.openlocfilehash: b3add86f011e016b1b6ea1a74f425f3f1deab002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700707"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="32e74-103">Integração de aplicativos de mensagens instantâneas ao Office</span><span class="sxs-lookup"><span data-stu-id="32e74-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="32e74-104">Este artigo descreve como configurar um aplicativo cliente de mensagens instantâneas para que ele se integre aos recursos de redes sociais no Office 2013, incluindo exibir presença e enviar mensagens instantâneas do cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="32e74-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="32e74-105">Se você tiver dúvidas ou comentários sobre este artigo técnico, ou sobre os processos que o descrevem, entre em contato diretamente com a Microsoft enviando um email para [docthis@microsoft.com](mailto:docthis@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="32e74-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="32e74-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="32e74-106">Introduction</span></span>
<span data-ttu-id="32e74-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-107"><a name="off15_IMIntegration_Intro"> </a></span></span>

<span data-ttu-id="32e74-108">O Office 2013 fornece integração avançada aos aplicativos cliente de mensagens instantâneas, incluindo o Lync 2013.</span><span class="sxs-lookup"><span data-stu-id="32e74-108">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="32e74-109">Essa integração fornece aos usuários recursos de mensagens instantâneas no Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 e OneNote 2013, bem como fornece integração de presença em páginas do SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="32e74-109">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="32e74-110">Os usuários podem ver a foto, o nome, o status de presença e os dados de contato das pessoas em sua lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="32e74-110">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="32e74-111">Elas podem começar uma sessão de mensagens instantâneas, chamadas de vídeo ou telefonemas diretamente do cartão de visita (o elemento da interface do usuário no Office 2013 que apresenta informações de contato e opções de comunicação).</span><span class="sxs-lookup"><span data-stu-id="32e74-111">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="32e74-112">Com o Office 2013, é fácil manter-se conectado aos seus contatos sem que você tenha que sair do email ou dos documentos em que está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="32e74-112">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32e74-113">Este artigo usa o termo aplicativo cliente de mensagens instantâneas para se referir especificamente ao aplicativo instalado no computador de um usuário que se comunica com o serviço de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-113">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="32e74-114">Por exemplo, o Lync 2013 é considerado um aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-114">For example, Lync 2013 is considered an IM client application.</span></span> <span data-ttu-id="32e74-115">Este artigo não fornece detalhes sobre como o aplicativo cliente de mensagens instantâneas se comunica com o serviço de mensagens instantâneas nem sobre o serviço em si.</span><span class="sxs-lookup"><span data-stu-id="32e74-115">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="32e74-116">Você pode personalizar um aplicativo cliente de mensagens instantâneas para que ele se comunique com o Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-116">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="32e74-117">Especificamente, é possível modificar o seu aplicativo de mensagens instantâneas para que ele exiba as seguintes informações na interface de usuário do Office:</span><span class="sxs-lookup"><span data-stu-id="32e74-117">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="32e74-118">Foto do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-118">Contact photo.</span></span>
    
- <span data-ttu-id="32e74-119">Nome do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-119">Contact name.</span></span>
    
- <span data-ttu-id="32e74-120">Nota de status pessoal do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="32e74-121">Status de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-121">Contact presence status.</span></span>
    
- <span data-ttu-id="32e74-122">Cadeia de disponibilidade do contato (por exemplo, "Disponível" ou "Ausência Temporária").</span><span class="sxs-lookup"><span data-stu-id="32e74-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="32e74-123">Cadeia de recursos do contato (por exemplo, "Pronto para Vídeo").</span><span class="sxs-lookup"><span data-stu-id="32e74-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="32e74-124">Início de mensagens instantâneas com um clique.</span><span class="sxs-lookup"><span data-stu-id="32e74-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="32e74-125">Início de chamada de vídeo com um clique.</span><span class="sxs-lookup"><span data-stu-id="32e74-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="32e74-126">Início de telefonema com um clique (incluindo SIP, número de telefone, caixa postal e ligar para novo número).</span><span class="sxs-lookup"><span data-stu-id="32e74-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="32e74-127">Gerenciamento de contatos (adicionar ao grupo de mensagens instantâneas).</span><span class="sxs-lookup"><span data-stu-id="32e74-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="32e74-128">Local e fuso horário do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="32e74-129">Dados, número de telefone, endereço de email, cargo e nome da empresa do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="32e74-130">**Figura 1. Cartão de visita no Office 2013**</span><span class="sxs-lookup"><span data-stu-id="32e74-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="32e74-131">![O Cartão de Pessoas no Office 2013](media/ocom15_peoplecard.png "O Cartão de Pessoas no Office 2013")</span><span class="sxs-lookup"><span data-stu-id="32e74-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="32e74-132">Para habilitar essa integração ao Office, um aplicativo cliente de mensagens instantâneas deve implementar um conjunto de interfaces que o Office fornece para se conectar a ele.</span><span class="sxs-lookup"><span data-stu-id="32e74-132">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="32e74-133">As APIs para essa integração estão incluídas no namespace [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) que está contido no arquivo Microsoft.Office.UC.dll, que é instalado com versões do Office 2013 que incluem o Lync/Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="32e74-133">The APIs for this integration are included in the [UCCollborationLib](https://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="32e74-134">O namespace **UCCollaborationLib** inclui as interfaces que você deve implementar para integração ao Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-134">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="32e74-135">A biblioteca de tipos para as interfaces necessárias está inserida no Lync 2013/Skype for Business.</span><span class="sxs-lookup"><span data-stu-id="32e74-135">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="32e74-136">Para integradores terceirizados, isso funcionará apenas quando o Lync 2013 e o Skype for Business estiverem instalados no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="32e74-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="32e74-137">Se estiver fazendo a integração usando o Office Standard, você precisará extrair a biblioteca de tipos e instalá-la no computador de destino.</span><span class="sxs-lookup"><span data-stu-id="32e74-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="32e74-138">O [SDK do Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) inclui o arquivo Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="32e74-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="32e74-139">Alguns aplicativos do Office 2010 podem se integrar de maneira semelhante a um aplicativo provedor de mensagens instantâneas de terceiros: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 e SharePoint Server 2010 (usando o controle ActiveX).</span><span class="sxs-lookup"><span data-stu-id="32e74-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="32e74-140">Muitas das etapas necessárias na integração do Office 2013 também se aplicam ao Office 2010.</span><span class="sxs-lookup"><span data-stu-id="32e74-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="32e74-141">Há várias diferenças importantes em como o Office 2010 se integra a um aplicativo do provedor de mensagens instantâneas:</span><span class="sxs-lookup"><span data-stu-id="32e74-141">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="32e74-142">O Office 2010 não exibe a foto do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-142">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="32e74-143">Você deve baixar o arquivo Microsoft.Office.Uc.dll separadamente do Office 2010.</span><span class="sxs-lookup"><span data-stu-id="32e74-143">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="32e74-144">O [SDK do Lync 2010](https://www.microsoft.com/en-us/download/details.aspx?id=18898) inclui o arquivo Microsoft.Office.UC.dll para Office 2010.</span><span class="sxs-lookup"><span data-stu-id="32e74-144">The [Lync 2010 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="32e74-145">Quando o aplicativo do Office chama o método [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) no aplicativo cliente de mensagens instantâneas, ele é passado na cadeia de caracteres "14.0.0.0".</span><span class="sxs-lookup"><span data-stu-id="32e74-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="32e74-146">O Office 2010 enumera todos os grupos e contatos assim que ele se conecta a um aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-146">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="32e74-147">Como o Office integra-se a um aplicativo cliente de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="32e74-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="32e74-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-148"><a name="off15_IMIntegration_How"> </a></span></span>

<span data-ttu-id="32e74-149">Quando um aplicativo do Office 2013 é iniciado, ele passa pelo seguinte processo para se integrar ao aplicativo cliente de mensagens instantâneas padrão:</span><span class="sxs-lookup"><span data-stu-id="32e74-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="32e74-150">Ele verifica o registro para descobrir o aplicativo cliente de mensagens instantâneas padrão e se conectar a ele.</span><span class="sxs-lookup"><span data-stu-id="32e74-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="32e74-151">Ele autentica-se no aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="32e74-152">Ele conecta-se a interfaces específicas que são expostas pelo aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="32e74-153">Ele determina os recursos do usuário atualmente conectado (usuário local), incluindo obter os contatos do usuário, determinar a presença do usuário e determinar os recursos de mensagens instantâneas do usuário (sistema de mensagens instantâneas, chat com vídeo, VOIP, etc.).</span><span class="sxs-lookup"><span data-stu-id="32e74-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="32e74-154">Ele obtém as informações de presença dos contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="32e74-155">Quando o aplicativo cliente de mensagens instantâneas é desligado, o aplicativo do Office 2013 é silenciosamente desconectado.</span><span class="sxs-lookup"><span data-stu-id="32e74-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="32e74-156">Como descobrir o aplicativo de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="32e74-156">Discovering the IM application</span></span>

<span data-ttu-id="32e74-157">O aplicativo do Office procura várias chaves e entradas específicas no registro para descobrir o aplicativo cliente de mensagens instantâneas padrão.</span><span class="sxs-lookup"><span data-stu-id="32e74-157">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="32e74-158">Se um aplicativo cliente de mensagens instantâneas padrão for descoberto, o aplicativo do Office tentará se conectar a ele.</span><span class="sxs-lookup"><span data-stu-id="32e74-158">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="32e74-159">O processo pelo qual o aplicativo do Office passa para descobrir o aplicativo cliente de mensagens instantâneas é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="32e74-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="32e74-160">O aplicativo do Office busca a subchave HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp no registro para verificar se ela está definida e lê o nome do aplicativo listado.</span><span class="sxs-lookup"><span data-stu-id="32e74-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="32e74-161">O aplicativo do Office lê a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning e monitora o valor das alterações.</span><span class="sxs-lookup"><span data-stu-id="32e74-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="32e74-162">O aplicativo do Office em seguida lê a chave do Registro HKEY_LOCAL_MACHINE\Software\IM Providers\ _Nome do aplicativo_ e obtém os valores de ProcessName e CLSID (ID de classe) armazenados nela.</span><span class="sxs-lookup"><span data-stu-id="32e74-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="32e74-163">Depois que o aplicativo cliente de mensagens instantâneas tiver concluído a sua sequência de inicialização com êxito e registrado todas as classes corretamente para a integração de presença, ele definirá a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning para "2", indicando que o aplicativo cliente está em execução.</span><span class="sxs-lookup"><span data-stu-id="32e74-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="32e74-164">Quando o aplicativo do Office descobrir que a chave HKEY_CURRENT_USER\Software\IM Providers\ _Nome do aplicativo_\UpAndRunning foi definida para "2", ele verificará a lista de processos em execução no computador em busca do nome do processo do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="32e74-165">Assim que o aplicativo do Office encontrar o processo que o aplicativo cliente de mensagens instantâneas usa, o aplicativo do Office chamará **CoCreateInstance** usando a CLSID para estabelecer uma conexão com o aplicativo cliente de mensagens instantâneas como um servidor COM fora do processo.</span><span class="sxs-lookup"><span data-stu-id="32e74-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="32e74-166">Autenticação da conexão com o aplicativo de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="32e74-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="32e74-167">Depois que o aplicativo do Office estabelecer uma conexão com o aplicativo cliente de mensagens instantâneas, o próximo passo será este:</span><span class="sxs-lookup"><span data-stu-id="32e74-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="32e74-168">O aplicativo do Office chama o método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) para verificar a interface [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="32e74-168">The Office application calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="32e74-169">O aplicativo do Office chama o método **IUCOfficeIntegration.GetAuthenticationInfo**, passando a versão mais alta de integração com suporte (por exemplo, "15.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="32e74-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="32e74-170">Se o aplicativo cliente de mensagens instantâneas der suporte à versão do Office passada como um parâmetro, o aplicativo retornará a seguinte cadeia de caracteres XML embutida em código para o código de chamada:</span><span class="sxs-lookup"><span data-stu-id="32e74-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="32e74-171">Por motivos de herança, o aplicativo cliente de mensagens instantâneas deverá retornar o valor exato `<authenticationinfo>` para a chamada a **GetAuthenticationInfo** se a versão do Office passada tiver suporte como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="32e74-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="32e74-172">Se o aplicativo cliente de mensagens instantâneas falhar ao retornar um valor, o aplicativo do Office chamará o método **GetAuthenticationInfo** novamente com a próxima versão mais alta com suporte do Office (por exemplo, "14.0.0.0").</span><span class="sxs-lookup"><span data-stu-id="32e74-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="32e74-173">Uma vez que o Office determina que o aplicativo cliente de mensagens instantâneas dá suporte às mensagens instantâneas e à integração de presença, ele se conecta a um conjunto necessário de interfaces para concluir a inicialização.</span><span class="sxs-lookup"><span data-stu-id="32e74-173">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="32e74-174">(Para saber mais, confira [Estabelecendo conexão com interfaces necessárias](#off15_IMIntegration_HowConnect)).</span><span class="sxs-lookup"><span data-stu-id="32e74-174">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="32e74-175">Se o aplicativo do Office encontrar um erro em qualquer uma das etapas acima, ele recuará e a integração de presença não será estabelecida novamente durante a sessão do aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="32e74-176">Como estabelecer conexão com as interfaces necessárias</span><span class="sxs-lookup"><span data-stu-id="32e74-176">Connecting to required interfaces</span></span>
<span data-ttu-id="32e74-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-177"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="32e74-178">Depois de autenticar a conexão com o aplicativo cliente de mensagens instantâneas, o aplicativo do Office tentará se conectar a um conjunto necessário de interfaces que o aplicativo cliente de mensagens instantâneas deve expor.</span><span class="sxs-lookup"><span data-stu-id="32e74-178">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="32e74-179">O aplicativo do Office faz isso seguindo este procedimento:</span><span class="sxs-lookup"><span data-stu-id="32e74-179">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="32e74-180">O aplicativo do Office obtém um objeto [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) chamando o método **IUCOfficeIntegration.GetInterface** e passando a constante **oiInterfaceLyncClient** da enumeração [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="32e74-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="32e74-181">O aplicativo do Office obtém um objeto [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) chamando o método **IUCOfficeIntegration.GetInterface** e passando a constante **oiInterfaceAutomation** da enumeração **OIInterface**.</span><span class="sxs-lookup"><span data-stu-id="32e74-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="32e74-182">O aplicativo do Office configura o ouvinte de eventos [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient).</span><span class="sxs-lookup"><span data-stu-id="32e74-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="32e74-183">O aplicativo do Office configura o ouvinte de eventos [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration).</span><span class="sxs-lookup"><span data-stu-id="32e74-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="32e74-184">O aplicativo do Office obtém o estado conectado do aplicativo cliente de mensagens instantâneas acessando a propriedade **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="32e74-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="32e74-185">O aplicativo do Office obtém os recursos do aplicativo cliente de mensagens instantâneas chamando o método **IUCOfficeIntegration.GetSupportedFeatures**, que retorna um sinalizador da enumeração [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="32e74-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="32e74-186">O aplicativo do Office acessa a propriedade **ILyncClient.Self** para obter uma referência a um objeto [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="32e74-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="32e74-187">Recuperação dos recursos do usuário local</span><span class="sxs-lookup"><span data-stu-id="32e74-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="32e74-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-188"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="32e74-189">O aplicativo do Office obtém os recursos do usuário local seguindo este procedimento:</span><span class="sxs-lookup"><span data-stu-id="32e74-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="32e74-190">Se o aplicativo cliente de mensagens instantâneas der suporte à interface **IClient2**, o Office tentará obter um objeto [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) acessando a propriedade **IClient2.PrivateContactManager**.</span><span class="sxs-lookup"><span data-stu-id="32e74-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="32e74-191">Se o aplicativo de mensagens instantâneas não der suporte à interface **IClient2**, o aplicativo do Office obterá um objeto **IContactManager** acessando a propriedade **ILyncClient.ContactManager**.</span><span class="sxs-lookup"><span data-stu-id="32e74-191">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="32e74-192">O aplicativo cliente de mensagens instantâneas deve retornar com êxito um objeto **IContactManager** para que qualquer outro recurso de mensagens instantâneas possa ser estabelecido.</span><span class="sxs-lookup"><span data-stu-id="32e74-192">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="32e74-193">O aplicativo do Office acessa a propriedade **ILyncClient.Uri** e, em seguida, chama **IContactManager.GetContactByUri** para obter o objeto [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) associado ao usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="32e74-194">O aplicativo do Office faz várias chamadas a **IContact.CanStart** para estabelecer os recursos do usuário local, passando os valores para **ModalityTypes.ucModalityInstantMessage** e **ModalityTypes.ucModalityAudioVideo** sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="32e74-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="32e74-195">Recuperação da presença do contato</span><span class="sxs-lookup"><span data-stu-id="32e74-195">Retrieving contact presence</span></span>
<span data-ttu-id="32e74-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-196"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="32e74-197">O aplicativo do Office obtém a presença do contato, incluindo o usuário local, seguindo este procedimento:</span><span class="sxs-lookup"><span data-stu-id="32e74-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="32e74-198">O aplicativo do Office chama **IContact.GetContactInformation** para obter um item de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="32e74-199">O aplicativo do Office, em seguida, faz a inscrição para receber alterações de status de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-199">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="32e74-200">Ele chama **IContactManager.CreateSubscription** para obter um objeto [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="32e74-200">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="32e74-201">Em seguida, ele chama **IContactSubscription.AddContact** para adicionar o contato à inscrição e chama **IContactSubscription.Subscribe** para obter as alterações no status do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-201">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="32e74-202">Se o aplicativo de mensagens instantâneas der suporte a **IContact2**, o Office tentará obter informações de presença chamando **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="32e74-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="32e74-203">O aplicativo do Office recupera as propriedades de presença para o contato chamando **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="32e74-203">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="32e74-204">O aplicativo do Office pode obter um segundo conjunto de propriedades de presença acessando a propriedade **IContact.Settings**.</span><span class="sxs-lookup"><span data-stu-id="32e74-204">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="32e74-205">Por fim, o aplicativo do Office obtém a associação a um grupo do contato acessando a propriedade **IContact.CustomGroups**.</span><span class="sxs-lookup"><span data-stu-id="32e74-205">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="32e74-206">Isso retorna uma coleção [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) que inclui todos os objetos [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) aos quais o contato pertence.</span><span class="sxs-lookup"><span data-stu-id="32e74-206">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="32e74-207">Desconexão do aplicativo de mensagens instantâneas</span><span class="sxs-lookup"><span data-stu-id="32e74-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="32e74-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-208"><a name="off15_IMIntegration_HowConnect"> </a></span></span>

<span data-ttu-id="32e74-209">Quando o aplicativo do Office 2013 detecta o evento **OnShuttingDown** do aplicativo de mensagens instantâneas, ele se desconecta silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="32e74-209">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="32e74-210">No entanto, se o aplicativo do Office for desligado antes do aplicativo de mensagens instantâneas, o aplicativo do Office não garantirá que a conexão seja limpa.</span><span class="sxs-lookup"><span data-stu-id="32e74-210">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="32e74-211">O aplicativo de mensagens instantâneas deve tratar dos vazamentos de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="32e74-211">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="32e74-212">Configuração de entradas e chaves do Registro</span><span class="sxs-lookup"><span data-stu-id="32e74-212">Setting registry keys and entries</span></span>
<span data-ttu-id="32e74-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-213"><a name="off15_IMIntegration_SetRegistry"> </a></span></span>

<span data-ttu-id="32e74-214">Conforme mencionado anteriormente, os aplicativos do Office 2013 compatíveis com mensagens instantâneas procuram chaves, entradas e valores específicos no registro para descobrir o aplicativo cliente de mensagens instantâneas ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="32e74-214">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="32e74-215">Esses valores de registro fornecem ao aplicativo do Office o nome do processo e a CLSID da classe que atua como o ponto de entrada para o modelo do aplicativo cliente de mensagens instantâneas (isto é, a classe que implementa a interface **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="32e74-215">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="32e74-216">O aplicativo do Office cria essa classe em conjunto e se conecta como um cliente ao servidor COM fora do processo no aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-216">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="32e74-217">Use a Tabela 1 para identificar as chaves, as entradas e os valores que devem ser gravados no registro para integração de um aplicativo cliente de mensagens instantâneas ao Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="32e74-218">**Table 1. Chaves do Registro para configuração do aplicativo cliente de mensagens instantâneas padrão**</span><span class="sxs-lookup"><span data-stu-id="32e74-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="32e74-219">**Chave**</span><span class="sxs-lookup"><span data-stu-id="32e74-219">**Key**</span></span>|<span data-ttu-id="32e74-220">**Entrada**</span><span class="sxs-lookup"><span data-stu-id="32e74-220">**Entry**</span></span>|<span data-ttu-id="32e74-221">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="32e74-221">**Type**</span></span>|<span data-ttu-id="32e74-222">**Valor**</span><span class="sxs-lookup"><span data-stu-id="32e74-222">**Value**</span></span>|<span data-ttu-id="32e74-223">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="32e74-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="32e74-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Nome do aplicativo\></span><span class="sxs-lookup"><span data-stu-id="32e74-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="32e74-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="32e74-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="32e74-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="32e74-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="32e74-227">O nome do aplicativo cliente de mensagens instantâneas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="32e74-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="32e74-228">Litware IM 2012</span><span class="sxs-lookup"><span data-stu-id="32e74-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="32e74-229">ProcessName</span><span class="sxs-lookup"><span data-stu-id="32e74-229">ProcessName</span></span>  <br/> |<span data-ttu-id="32e74-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="32e74-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="32e74-231">O nome do processo do aplicativo cliente de mensagens instantâneas de terceiros.</span><span class="sxs-lookup"><span data-stu-id="32e74-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="32e74-232">litware.exe</span><span class="sxs-lookup"><span data-stu-id="32e74-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="32e74-233">GUID</span><span class="sxs-lookup"><span data-stu-id="32e74-233">GUID</span></span>  <br/> |<span data-ttu-id="32e74-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="32e74-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="32e74-235">Uma ID de classe (CLSID) para a classe raiz que pode ser criada em conjunto no aplicativo cliente de mensagens instantâneas (a classe que implementa a interface **IUCOfficeIntegration**).</span><span class="sxs-lookup"><span data-stu-id="32e74-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="32e74-236">(UM GUID)</span><span class="sxs-lookup"><span data-stu-id="32e74-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="32e74-237">HKEY_CURRENT_USER\Software\IM Providers</span><span class="sxs-lookup"><span data-stu-id="32e74-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="32e74-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="32e74-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="32e74-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="32e74-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="32e74-240">O nome do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-240">The name of the IM client application.</span></span> <span data-ttu-id="32e74-241">Deve ser igual ao nome da chave do Registro de nível superior (hive) em HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="32e74-241">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="32e74-242">Litware</span><span class="sxs-lookup"><span data-stu-id="32e74-242">Litware</span></span>  <br/> |
|<span data-ttu-id="32e74-243">HKEY_CURRENT_USER\Software\IM Providers\\<Nome do aplicativo\></span><span class="sxs-lookup"><span data-stu-id="32e74-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="32e74-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="32e74-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="32e74-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="32e74-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="32e74-246">Um valor inteiro entre 0 e 2:</span><span class="sxs-lookup"><span data-stu-id="32e74-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="32e74-247">0 – Não está em execução</span><span class="sxs-lookup"><span data-stu-id="32e74-247">0—Not running</span></span>  <br/>  <span data-ttu-id="32e74-248">1 – Iniciando</span><span class="sxs-lookup"><span data-stu-id="32e74-248">1—Starting</span></span>  <br/>  <span data-ttu-id="32e74-249">2 – Executando</span><span class="sxs-lookup"><span data-stu-id="32e74-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="32e74-250">**OBSERVAÇÃO**: a chave do Registro do nome do aplicativo deve ser igual ao valor da entrada DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="32e74-250">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="32e74-251">Como implementar as interfaces necessárias para integração ao Office</span><span class="sxs-lookup"><span data-stu-id="32e74-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="32e74-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span></span>

<span data-ttu-id="32e74-253">Há três interfaces no namespace **UCCollaborationLib** que o executável (ou servidor COM) de um aplicativo cliente de mensagens instantâneas deve implementar para que possa se integrar ao Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-253">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="32e74-254">Se essas interfaces não estiverem implementadas, o aplicativo do Office recuará durante o processo de inicialização e a conexão com o aplicativo cliente de mensagens instantâneas não será estabelecida.</span><span class="sxs-lookup"><span data-stu-id="32e74-254">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="32e74-255">As interfaces necessárias são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="32e74-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="32e74-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration): embora não seja necessária, a interface **_IUCOfficeIntegrationEvents** também deve ser implementada na mesma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="32e74-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="32e74-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient): embora não seja necessária, a interface **_ILyncClientEvents** também deve ser implementada na mesma classe derivada.</span><span class="sxs-lookup"><span data-stu-id="32e74-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="32e74-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="32e74-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="32e74-259">Interface IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="32e74-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="32e74-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span></span>

<span data-ttu-id="32e74-261">A interface **IUCOfficeIntegration** fornece o ponto de entrada para que um aplicativo do Office se conecte ao aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-261">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="32e74-262">A interface define três métodos que um aplicativo do Office chama como parte do processo de iniciar uma conexão com o aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-262">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="32e74-263">A classe que implementa a interface **IUCOfficeIntegration** deve ser criada em conjunto para que o Office possa criar uma instância dela em conjunto.</span><span class="sxs-lookup"><span data-stu-id="32e74-263">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="32e74-264">Além disso, ela deve expor a CLSID que é inserida como o valor para a entrada GUID na chave do Registro HKEY_LOCAL_MACHINE\Software\IM Providers\  _Nome do aplicativo_.</span><span class="sxs-lookup"><span data-stu-id="32e74-264">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="32e74-265">A classe que é herdada de **IUCOfficeIntegration** também deve implementar a interface **_IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="32e74-265">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="32e74-266">A interface **_IUCOfficeIntegrationEvents** contém os membros que expõem os manipuladores de eventos da interface **IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="32e74-266">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="32e74-267">A Tabela 2 mostra os membros que devem ser implementados na classe que é herdada de **IUCOfficeIntegration** e **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="32e74-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-268">Para saber mais sobre as interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegrationEvents** e seus membros, confira [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) e [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="32e74-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](https://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="32e74-269">**Tabela 2. Implementação das interfaces IUCOfficeIntegration e _IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="32e74-270">**Interface**</span><span class="sxs-lookup"><span data-stu-id="32e74-270">**Interface**</span></span>|<span data-ttu-id="32e74-271">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-271">**Member**</span></span>|<span data-ttu-id="32e74-272">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32e74-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="32e74-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="32e74-274">Método **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="32e74-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="32e74-275">Obtém a cadeia de caracteres de informações sobre a autenticação.</span><span class="sxs-lookup"><span data-stu-id="32e74-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="32e74-276">Método **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="32e74-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="32e74-277">Obtém a interface de uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="32e74-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="32e74-278">Método **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="32e74-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="32e74-279">Obtém os recursos de integração do Office com suporte.</span><span class="sxs-lookup"><span data-stu-id="32e74-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="32e74-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="32e74-281">Evento **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="32e74-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="32e74-282">O evento gerado quando o aplicativo cliente de mensagens instantâneas está tentando desligar.</span><span class="sxs-lookup"><span data-stu-id="32e74-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="32e74-283">Use o código a seguir para definir uma classe que é herdada das interfaces **IUCOfficeIntegration** e **_IUCOfficeIntegration** em um aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
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

<span data-ttu-id="32e74-284">O método **GetAuthenticationInfo** usa uma cadeia de caracteres como um argumento para o parâmetro _version_.</span><span class="sxs-lookup"><span data-stu-id="32e74-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="32e74-285">Quando o aplicativo do Office chama esse método, ele passa uma das duas cadeias de caracteres para o argumento, dependendo da versão do Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="32e74-286">Quando o aplicativo do Office fornece o método com a versão do Office que tem suporte do aplicativo cliente de mensagens instantâneas (isto é, dá suporte à funcionalidade), o método **GetAuthenticationInfo** retorna uma cadeia de XML embutida em código `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="32e74-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="32e74-287">Use o código a seguir para implementar o método **GetAuthentication** no código do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="32e74-288">O método **GetInterface** leva e traz referências a classes para o código de chamada, dependendo do que é passado como um argumento para o parâmetro _interface_.</span><span class="sxs-lookup"><span data-stu-id="32e74-288">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="32e74-289">Quando um aplicativo do Office chama o método **GetInterface**, ele passa um dos dois valores para o parâmetro interface: ou a constante **oiInterfaceILyncClient** (1) ou a constante **oiInterfaceIAutomation** (2) da enumeração [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface).</span><span class="sxs-lookup"><span data-stu-id="32e74-289">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](https://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="32e74-290">Se o aplicativo do Office passar a constante **oiInterfaceILyncClient**, o método **GetInterface** retornará uma referência a uma classe que implementa a interface **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="32e74-290">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="32e74-291">Se o aplicativo do Office passar a constante **oiInterfaceIAutomation**, o método **GetInterface** retornará uma classe que implementa a interface **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="32e74-291">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="32e74-292">Use o exemplo de código a seguir para implementar o método **GetInterface** no código do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
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

<span data-ttu-id="32e74-293">O método **GetSupportedFeatures** retorna informações sobre os recursos de mensagens instantâneas aos quais o aplicativo cliente de mensagens instantâneas dá suporte.</span><span class="sxs-lookup"><span data-stu-id="32e74-293">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="32e74-294">Ele usa uma cadeia de caracteres para seu único parâmetro, _version_.</span><span class="sxs-lookup"><span data-stu-id="32e74-294">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="32e74-295">Quando o aplicativo do Office chama o método **GetSupportFeatures**, o método retorna um valor da enumeração [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature).</span><span class="sxs-lookup"><span data-stu-id="32e74-295">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](https://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="32e74-296">O valor retornado especifica os recursos do cliente de mensagens instantâneas, onde cada recurso do aplicativo cliente de mensagens instantâneas é indicado para o aplicativo do Office adicionando um sinalizador ao valor.</span><span class="sxs-lookup"><span data-stu-id="32e74-296">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="32e74-297">Os aplicativos do Office 2013 ignoram as seguintes constantes na enumeração **OIFeature**:</span><span class="sxs-lookup"><span data-stu-id="32e74-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="32e74-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="32e74-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="32e74-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="32e74-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="32e74-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="32e74-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="32e74-301">Use o exemplo de código a seguir para implementar o método **GetSupportFeatures** no código do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="32e74-302">Interface ILyncClient</span><span class="sxs-lookup"><span data-stu-id="32e74-302">ILyncClient interface</span></span>
<span data-ttu-id="32e74-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span></span>

<span data-ttu-id="32e74-304">A interface **ILyncClient** é mapeada para os recursos do aplicativo cliente de mensagens instantâneas em si.</span><span class="sxs-lookup"><span data-stu-id="32e74-304">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="32e74-305">Ela expõe propriedades que se referem à pessoa que está conectada ao aplicativo (o usuário local, representado pela interface [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf)), o estado do aplicativo, a lista de contatos do usuário local e várias outras configurações.</span><span class="sxs-lookup"><span data-stu-id="32e74-305">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](https://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="32e74-306">Quando está tentando se conectar ao aplicativo cliente de mensagens instantâneas, o aplicativo do Office obtém uma referência a um objeto que implementa a interface **ILyncClient**.</span><span class="sxs-lookup"><span data-stu-id="32e74-306">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="32e74-307">Dessa referência, o Office pode acessar muitas funcionalidades do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-307">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="32e74-308">Além disso, a classe que implementa a interface **ILyncClient** também deve implementar a interface **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="32e74-308">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="32e74-309">A interface **_ILyncClientEvents** expõe vários eventos que são obrigatórios para monitoramento do estado do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-309">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="32e74-310">A Tabela 3 mostra os membros que devem ser implementados na classe que é herdade de **ILyncClient** e **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="32e74-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-311">Qualquer membro da interface **ILyncClient** ou **\_ILyncClientEvents** não listado na tabela deve estar presente, mas não precisa ser implementada.</span><span class="sxs-lookup"><span data-stu-id="32e74-311">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-312">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-312">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="32e74-313">Para saber mais sobre as interfaces **ILyncClient** e **_ILyncClientEvents** e seus membros, confira [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) e [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="32e74-313">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](https://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](https://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="32e74-314">**Tabela 3. Implementação das interfaces ILyncClient e ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="32e74-315">**Interface**</span><span class="sxs-lookup"><span data-stu-id="32e74-315">**Interface**</span></span>|<span data-ttu-id="32e74-316">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-316">**Member**</span></span>|<span data-ttu-id="32e74-317">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32e74-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="32e74-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="32e74-319">Propriedade **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="32e74-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="32e74-320">Obtém o gerenciador do grupo de contatos.</span><span class="sxs-lookup"><span data-stu-id="32e74-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="32e74-321">Propriedade **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="32e74-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="32e74-322">Obtém o gerenciador de conversas.</span><span class="sxs-lookup"><span data-stu-id="32e74-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="32e74-323">Propriedade **Self**</span><span class="sxs-lookup"><span data-stu-id="32e74-323">**Self** property</span></span>  <br/> |<span data-ttu-id="32e74-324">Obtém o objeto **Self**.</span><span class="sxs-lookup"><span data-stu-id="32e74-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="32e74-325">Método **SignIn**</span><span class="sxs-lookup"><span data-stu-id="32e74-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="32e74-326">Inicia o processo de entrada do aplicativo cliente de mensagens instantâneas com uma disponibilidade específica.</span><span class="sxs-lookup"><span data-stu-id="32e74-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="32e74-327">Propriedade **State**</span><span class="sxs-lookup"><span data-stu-id="32e74-327">**State** property</span></span>  <br/> |<span data-ttu-id="32e74-328">Obtém o estado atual da plataforma.</span><span class="sxs-lookup"><span data-stu-id="32e74-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="32e74-329">Propriedade **Uri**</span><span class="sxs-lookup"><span data-stu-id="32e74-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="32e74-330">Obtém o URI do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="32e74-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="32e74-332">Evento **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="32e74-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="32e74-333">Gerado quando o estado do aplicativo cliente de mensagens instantâneas muda.</span><span class="sxs-lookup"><span data-stu-id="32e74-333">Raised when the IM client application state changes.</span></span> <span data-ttu-id="32e74-334">Você deve tratar esse evento e obter a propriedade **eventData.NewState**.</span><span class="sxs-lookup"><span data-stu-id="32e74-334">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="32e74-335">O evento é gerado para todos os processos vinculados a uma instância de um aplicativo cliente de mensagens instantâneas quando qualquer subsistema no aplicativo faz com que o estado mude.</span><span class="sxs-lookup"><span data-stu-id="32e74-335">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="32e74-336">Durante o processo de inicialização, o Office acessa a propriedade **ILyncClient.State**.</span><span class="sxs-lookup"><span data-stu-id="32e74-336">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="32e74-337">Essa propriedade precisa retornar um valor da enumeração [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState).</span><span class="sxs-lookup"><span data-stu-id="32e74-337">This property needs to return a value from the [UCCollaborationLib.ClientState](https://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
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

<span data-ttu-id="32e74-338">A propriedade **State** armazena o status atual do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-338">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="32e74-339">Ela deve ser definida e atualizada durante toda a sessão de aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-339">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="32e74-340">Quando o aplicativo cliente de mensagens instantâneas é conectado, desconectado ou desligado, ele deve definir a propriedade **State**.</span><span class="sxs-lookup"><span data-stu-id="32e74-340">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="32e74-341">É melhor definir essa propriedade nos métodos **ILyncClient.SignIn** e **ILyncClient.SignOut**, como demonstra o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="32e74-341">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
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

<span data-ttu-id="32e74-342">O exemplo de código a seguir demonstra como configurar o ouvinte de eventos usando as interfaces _ **ILyncClientEvents** e _ **IUCOfficeIntegrationEvents**.</span><span class="sxs-lookup"><span data-stu-id="32e74-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
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

### <a name="iautomation-interface"></a><span data-ttu-id="32e74-343">Interface IAutomation</span><span class="sxs-lookup"><span data-stu-id="32e74-343">IAutomation interface</span></span>
<span data-ttu-id="32e74-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span></span>

<span data-ttu-id="32e74-345">A interface **IAutomation** automatiza recursos do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-345">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="32e74-346">Ela pode ser usada para iniciar conversas, ingressar em conferências e fornecem contexto da janela de extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="32e74-346">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="32e74-347">A Tabela 4 mostra os membros que devem ser implementados na classe que é herdada de **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="32e74-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-348">Qualquer membro da interface **IAutomation** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-349">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="32e74-350">Para saber mais sobre a interface **IAutomation** e seus membros, confira [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="32e74-350">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](https://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="32e74-351">**Tabela 4. Implementação da interface IAutomation**</span><span class="sxs-lookup"><span data-stu-id="32e74-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="32e74-352">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-352">**Member**</span></span>|<span data-ttu-id="32e74-353">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-354">Método **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="32e74-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="32e74-355">Inicia uma conversa usando a modalidade de conversa especificada.</span><span class="sxs-lookup"><span data-stu-id="32e74-355">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="32e74-356">Uma instância de **IConversationWindow** é retornada.</span><span class="sxs-lookup"><span data-stu-id="32e74-356">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="32e74-357">Como implementar a integração da presença do contato</span><span class="sxs-lookup"><span data-stu-id="32e74-357">Implementing contact presence integration</span></span>
<span data-ttu-id="32e74-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span></span>

<span data-ttu-id="32e74-359">Além das três interfaces obrigatórias abordadas anteriormente, há várias outras interfaces que são importantes para habilitar a funcionalidade de presença do contato no Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-359">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="32e74-360">Elas incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="32e74-360">These include the following:</span></span>
  
- <span data-ttu-id="32e74-361">A interface [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) ou **IContact2**.</span><span class="sxs-lookup"><span data-stu-id="32e74-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="32e74-362">A interface [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf).</span><span class="sxs-lookup"><span data-stu-id="32e74-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="32e74-363">As interfaces [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) e [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager).</span><span class="sxs-lookup"><span data-stu-id="32e74-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="32e74-364">As interfaces [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) e [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup).</span><span class="sxs-lookup"><span data-stu-id="32e74-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="32e74-365">A interface [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="32e74-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="32e74-366">A interface [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint).</span><span class="sxs-lookup"><span data-stu-id="32e74-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="32e74-367">A interface [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="32e74-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="32e74-368">Interface IContact</span><span class="sxs-lookup"><span data-stu-id="32e74-368">IContact interface</span></span>
<span data-ttu-id="32e74-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span></span>

<span data-ttu-id="32e74-370">A interface **IContact** representa um usuário do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-370">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="32e74-371">A interface expõe presença, modalidades disponíveis, associação a um grupo e propriedades do tipo de contato de um usuário.</span><span class="sxs-lookup"><span data-stu-id="32e74-371">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="32e74-372">Para iniciar uma conversa com outro usuário, você deve fornecer a instância de usuário de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="32e74-372">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="32e74-373">A Tabela 5 mostra os membros que devem ser implementados na classe que é herdada de **IContact**.</span><span class="sxs-lookup"><span data-stu-id="32e74-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-374">Qualquer membro da interface **IContact** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-375">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="32e74-376">Para saber mais sobre a interface **IContact** e seus membros, confira [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="32e74-376">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](https://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="32e74-377">**Tabela 5. Implementação da interface IContact**</span><span class="sxs-lookup"><span data-stu-id="32e74-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="32e74-378">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-378">**Member**</span></span>|<span data-ttu-id="32e74-379">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-380">Método **CanStart**</span><span class="sxs-lookup"><span data-stu-id="32e74-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="32e74-381">Retornará **true** se um determinado tipo de modalidade puder ser iniciado no contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="32e74-382">Método **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="32e74-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="32e74-383">Obtém um item de presença de um contato de publicação.</span><span class="sxs-lookup"><span data-stu-id="32e74-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="32e74-384">Método **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="32e74-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="32e74-385">Obtém vários itens de presença de um contato de publicação.</span><span class="sxs-lookup"><span data-stu-id="32e74-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="32e74-386">Propriedade **Settings**</span><span class="sxs-lookup"><span data-stu-id="32e74-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="32e74-387">Obtém uma coleção de propriedades do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="32e74-388">Propriedade **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="32e74-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="32e74-389">Obtém uma coleção de grupos dos quais o contato é um membro.</span><span class="sxs-lookup"><span data-stu-id="32e74-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="32e74-390">Durante o processo de inicialização, o aplicativo do Office chama o método **IContact.CanStart** para determinar os recursos de mensagens instantâneas para o usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-390">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="32e74-391">O método **CanStart** usa um sinalizador da enumeração [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) como um argumento para o parâmetro __modalityTypes_.</span><span class="sxs-lookup"><span data-stu-id="32e74-391">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](https://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter.</span></span> <span data-ttu-id="32e74-392">Se o usuário atual puder se envolver na modalidade solicitada (isto é, o usuário pode enviar e receber mensagens instantâneas, mensagens de áudio e vídeo ou compartilhar aplicativos), o método **CanStart** retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="32e74-392">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
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

<span data-ttu-id="32e74-393">O método **GetContactInformation** recupera informações sobre o contato do objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="32e74-393">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="32e74-394">O código de chamada precisa passar um valor da enumeração [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) para o parâmetro __contactInformationType_, que indica os dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="32e74-394">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](https://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
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

<span data-ttu-id="32e74-395">Semelhante a **GetContactInformation**, o método **BatchGetContactInformation** recupera vários itens de presença sobre o contato no objeto **IContact**.</span><span class="sxs-lookup"><span data-stu-id="32e74-395">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="32e74-396">O código de chamada precisa passar uma matriz de valores da enumeração **ContactInformationType** para o parâmetro __contactInformationTypes_.</span><span class="sxs-lookup"><span data-stu-id="32e74-396">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter.</span></span> <span data-ttu-id="32e74-397">O método retorna um objeto [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) que contém os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="32e74-397">The method returns an [UCCollaborationLib.IContactInformationDictionary](https://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
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

<span data-ttu-id="32e74-398">A propriedade **IContact.Settings** retorna um objeto **IContactSettingDictionary** que contém propriedades personalizadas sobre o contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
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

<span data-ttu-id="32e74-399">A propriedade **IContact.CustomGroups** retorna um objeto **IGroupCollection** que inclui todos os grupos dos quais o contato é um membro.</span><span class="sxs-lookup"><span data-stu-id="32e74-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
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

### <a name="iself-interface"></a><span data-ttu-id="32e74-400">Interface ISelf</span><span class="sxs-lookup"><span data-stu-id="32e74-400">ISelf interface</span></span>
<span data-ttu-id="32e74-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span></span>

<span data-ttu-id="32e74-402">Durante o processo de inicialização, o aplicativo do Office obtém os dados para o usuário atual acessando a propriedade **ILyncClient.Self**, que deve retornar um objeto **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="32e74-402">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="32e74-403">A interface **ISelf** representa o local, o usuário do aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-403">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="32e74-404">A Tabela 6 mostra os membros que devem ser implementados na classe que é herdada de **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="32e74-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-405">Qualquer membro da interface **ISelf** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-405">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-406">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-406">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="32e74-407">**Tabela 6. Implementação da interface ISelf**</span><span class="sxs-lookup"><span data-stu-id="32e74-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="32e74-408">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-408">**Member**</span></span>|<span data-ttu-id="32e74-409">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-410">Propriedade **Contact**</span><span class="sxs-lookup"><span data-stu-id="32e74-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="32e74-411">Obtém o objeto **IContact** associado ao usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="32e74-412">Presença, modalidades disponíveis, associação a um grupo e propriedades do tipo de contato para o usuário local são expostos pela propriedade **ISelf.Contact** (que retorna um objeto **IContact**).</span><span class="sxs-lookup"><span data-stu-id="32e74-412">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="32e74-413">Durante o processo de inicialização, o aplicativo do Office acessa a propriedade **ISelf.Contact** para obter uma referência às informações de contato para o usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-413">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="32e74-414">Use o código a seguir para definir uma classe que seja herdada da interface **ISelf** que implementa a propriedade **Contact**.</span><span class="sxs-lookup"><span data-stu-id="32e74-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
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

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="32e74-415">Interfaces IContactManager e _IContactManagerEvents</span><span class="sxs-lookup"><span data-stu-id="32e74-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="32e74-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span></span>

<span data-ttu-id="32e74-417">O objeto **IContactManager** gerencia os contatos para o usuário local, incluindo as informações de contato do próprio usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-417">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="32e74-418">O aplicativo do Office usa um objeto **IContactManager** para acessar objetos **IContact** que correspondem aos contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-418">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="32e74-419">A Tabela 7 mostra os membros que devem ser implementados na classe que é herdada de **IContactManager** e **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="32e74-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-420">Qualquer membro da interface **IContactManager** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-421">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E\_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-421">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="32e74-422">Para saber mais sobre as interfaces **IContactManager** e **_IContactManagerEvents** e seus membros, confira [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) e [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="32e74-422">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](https://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](https://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="32e74-423">**Tabela 7. Implementação das interfaces IContactManager e _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="32e74-424">**Interface**</span><span class="sxs-lookup"><span data-stu-id="32e74-424">**Interface**</span></span>|<span data-ttu-id="32e74-425">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-425">**Member**</span></span>|<span data-ttu-id="32e74-426">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32e74-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="32e74-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="32e74-428">Método **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="32e74-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="32e74-429">Encontra ou cria uma nova instância de contato usando o URI de contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="32e74-430">Método **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="32e74-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="32e74-431">Cria um objeto **ISubscription** que pode ser usado para envio em lotes de inscrições ou consultas.</span><span class="sxs-lookup"><span data-stu-id="32e74-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="32e74-432">Método **Lookup**</span><span class="sxs-lookup"><span data-stu-id="32e74-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="32e74-433">Procura um contato ou grupo de distribuição.</span><span class="sxs-lookup"><span data-stu-id="32e74-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="32e74-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="32e74-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="32e74-435">Evento **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="32e74-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="32e74-436">Gerado quando um grupo é adicionado a uma coleção de grupos.</span><span class="sxs-lookup"><span data-stu-id="32e74-436">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="32e74-437">A coleção de grupos atualizados pode ser obtida na propriedade **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="32e74-437">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="32e74-438">Evento **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="32e74-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="32e74-439">Gerado quando um grupo é removido de uma coleção de grupos.</span><span class="sxs-lookup"><span data-stu-id="32e74-439">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="32e74-440">A coleção de grupos atualizados pode ser obtida na propriedade **IContactManager.Groups**.</span><span class="sxs-lookup"><span data-stu-id="32e74-440">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="32e74-441">Evento **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="32e74-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="32e74-442">Gerado quando o status de um provedor de pesquisa muda.</span><span class="sxs-lookup"><span data-stu-id="32e74-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="32e74-443">O Office chama **IContactManager.GetContactByUri** para obter informações de presença de um contato usando o endereço SIP do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-443">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="32e74-444">Quando um contato é configurado para um endereço SIP no Active Directory, o Office determina esse endereço para um contato e chama **GetContactByUri**, passando o endereço SIP do contato para o parâmetro __contactUri_.</span><span class="sxs-lookup"><span data-stu-id="32e74-444">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="32e74-445">Quando o Office não puder determinar o endereço SIP para o contato, ele chamará o método **IContactManager.Lookup** para encontrar o SIP usando o serviço de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-445">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="32e74-446">Aqui, o Office passa os melhores dados que pode encontrar para o contato (por exemplo, o endereço de email do contato).</span><span class="sxs-lookup"><span data-stu-id="32e74-446">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="32e74-447">O método **Lookup** retorna um objeto **AsynchronousOperation** de modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="32e74-447">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="32e74-448">Quando invocar o retorno de chamada, o método **Lookup** deverá retornar o êxito ou a falha da operação além do URI do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-448">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
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

<span data-ttu-id="32e74-449">O aplicativo do Office precisa ser inscrito para receber as alterações de presença de um contato individual.</span><span class="sxs-lookup"><span data-stu-id="32e74-449">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="32e74-450">Dessa forma, quando o status de presença de um contato é alterado, o servidor de mensagens instantâneas alerta o aplicativo cliente de mensagens instantâneas, alertando, assim, o aplicativo do Office.</span><span class="sxs-lookup"><span data-stu-id="32e74-450">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="32e74-451">Para isso, o aplicativo do Office chama o método **IContactManager.CreateSubscription** para criar um novo objeto **IContactSubscription** para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="32e74-451">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
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

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="32e74-452">Interfaces IGroup e IGroupCollection</span><span class="sxs-lookup"><span data-stu-id="32e74-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="32e74-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span></span>

<span data-ttu-id="32e74-454">O objeto **IGroup** representa uma coleção de contatos com propriedades adicionais para identificar a coleção de contatos por um nome de grupo coletivo.</span><span class="sxs-lookup"><span data-stu-id="32e74-454">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="32e74-455">Um objeto **IGroupCollection** representa uma coleção de objetos **IGroup** definidos por um usuário local e o aplicativo cliente de mensagens instantâneas.</span><span class="sxs-lookup"><span data-stu-id="32e74-455">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="32e74-456">O aplicativo do Office usa os objetos **IGroupCollection** e **IGroup** para acessar os contatos do usuário local.</span><span class="sxs-lookup"><span data-stu-id="32e74-456">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="32e74-457">A Tabela 9 mostra os membros que devem ser implementados nas classes que são herdadas de **IGroup** e **IGroupCollection** na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="32e74-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="32e74-458">Qualquer membro da interface **IGroup** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-459">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="32e74-460">Para saber mais sobre as interfaces **IGroup** e **IGroupCollection** e seus membros, confira [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) e [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="32e74-460">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](https://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](https://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="32e74-461">**Tabela 9. Implementação das interfaces IGroup e IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="32e74-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="32e74-462">**Interface**</span><span class="sxs-lookup"><span data-stu-id="32e74-462">**Interface**</span></span>|<span data-ttu-id="32e74-463">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-463">**Member**</span></span>|<span data-ttu-id="32e74-464">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32e74-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="32e74-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="32e74-466">Propriedade **Count**</span><span class="sxs-lookup"><span data-stu-id="32e74-466">**Count** property</span></span>  <br/> |<span data-ttu-id="32e74-467">Retorna a contagem dos objetos **IGroup** na coleção</span><span class="sxs-lookup"><span data-stu-id="32e74-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="32e74-468">Propriedade **Item**</span><span class="sxs-lookup"><span data-stu-id="32e74-468">**Item** property</span></span>  <br/> |<span data-ttu-id="32e74-469">Retorna o objeto **IGroup** no índice especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="32e74-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="32e74-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="32e74-470">**IGroup**</span></span> <br/> |<span data-ttu-id="32e74-471">Propriedade **Id**</span><span class="sxs-lookup"><span data-stu-id="32e74-471">**Id** property</span></span>  <br/> |<span data-ttu-id="32e74-472">Retorna a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="32e74-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="32e74-473">Quando o aplicativo do Office obtém informações do usuário local, ele acessa as associações ao grupo do contato (usuário local) chamando a propriedade **IContact.CustomGroups**, que retorna um objeto **IGroupCollection**.</span><span class="sxs-lookup"><span data-stu-id="32e74-473">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="32e74-474">O **IGroupCollection** deve conter uma matriz (ou **Lista**) de objetos **IGroup**.</span><span class="sxs-lookup"><span data-stu-id="32e74-474">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="32e74-475">A classe que deriva de **IGroupCollection** deve expor uma propriedade **Count**, que retorna o número de itens na coleção, e um método indexador, **this(int)**, que retorna um objeto **IGroup** da coleção.</span><span class="sxs-lookup"><span data-stu-id="32e74-475">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="32e74-476">Interface IContactSubscription</span><span class="sxs-lookup"><span data-stu-id="32e74-476">IContactSubscription interface</span></span>
<span data-ttu-id="32e74-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span></span>

<span data-ttu-id="32e74-478">A interface **IContactSubscription** permite especificar os contatos que receberão atualizações das informações de presença e os tipos de informações de presença que disparam uma notificação.</span><span class="sxs-lookup"><span data-stu-id="32e74-478">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="32e74-479">Os aplicativos do Office usam um objeto **IContactSubscription** para registrar alterações no status de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-479">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="32e74-480">A Tabela 10 mostra os membros que devem ser implementados nas classes que são herdadas de **IContactSubscription**.</span><span class="sxs-lookup"><span data-stu-id="32e74-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-481">Qualquer membro da interface **IContactSubscription** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-482">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="32e74-483">Para saber mais sobre a interface **IContactSubscription** e seus membros, confira [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="32e74-483">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](https://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="32e74-484">**Tabela 10. Implementação da interface IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="32e74-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="32e74-485">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-485">**Member**</span></span>|<span data-ttu-id="32e74-486">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-487">Método **AddContact**</span><span class="sxs-lookup"><span data-stu-id="32e74-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="32e74-488">Adiciona um contato ao objeto de inscrição.</span><span class="sxs-lookup"><span data-stu-id="32e74-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="32e74-489">Método **Subscribe**</span><span class="sxs-lookup"><span data-stu-id="32e74-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="32e74-490">Ajuda o aplicativo cliente de mensagens instantâneas a monitorar a presença de um contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="32e74-491">A interface **IContactSubscription** deve conter uma referência a todos os objetos **IContact** que ela monitora, usando uma matriz ou uma **Lista**.</span><span class="sxs-lookup"><span data-stu-id="32e74-491">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="32e74-492">O método **IContactSubscription.AddContact** é adicionado para um objeto **IContact** à estrutura de dados subjacente do objeto **IContactSubscription**, adicionando, assim, um novo contato a ser monitorado em busca de alterações de presença.</span><span class="sxs-lookup"><span data-stu-id="32e74-492">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="32e74-493">O método **IContactSubscription.Subscribe** permite que um aplicativo cliente de mensagens instantâneas acesse observadores de presença do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-493">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="32e74-494">Ele pode usar a estratégia de sondagem para obter a presença do servidor dos contatos nos quais o aplicativo cliente de mensagens instantâneas se inscreveu.</span><span class="sxs-lookup"><span data-stu-id="32e74-494">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="32e74-495">O método **Subscribe** é útil em situações em que a presença é solicitada para alguém fora da lista de contatos de um usuário (por exemplo, de uma rede pública maior).</span><span class="sxs-lookup"><span data-stu-id="32e74-495">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="32e74-496">Interface IContactEndPoint</span><span class="sxs-lookup"><span data-stu-id="32e74-496">IContactEndPoint interface</span></span>
<span data-ttu-id="32e74-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span></span>

<span data-ttu-id="32e74-498">A **IContactEndPoint** representa um número de telefone de uma coleção de números de telefone de um contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="32e74-499">A Tabela 11 mostra os membros que devem ser implementados nas classes que são herdadas de **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="32e74-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-500">Qualquer membro da interface **IContactEndPoint** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-501">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="32e74-502">Para saber mais sobre a interface **IContactEndPoint** e seus membros, confira [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="32e74-502">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](https://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="32e74-503">**Tabela 11. Implementação da interface IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="32e74-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="32e74-504">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-504">**Member**</span></span>|<span data-ttu-id="32e74-505">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-506">Propriedade **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="32e74-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="32e74-507">Obtém a cadeia de caracteres de exibição.</span><span class="sxs-lookup"><span data-stu-id="32e74-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="32e74-508">Propriedade **Type**</span><span class="sxs-lookup"><span data-stu-id="32e74-508">**Type** property</span></span>  <br/> |<span data-ttu-id="32e74-509">Obtém o tipo de ponto de extremidade do contato</span><span class="sxs-lookup"><span data-stu-id="32e74-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="32e74-510">Propriedade **Uri**</span><span class="sxs-lookup"><span data-stu-id="32e74-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="32e74-511">Obtém URI do contato.</span><span class="sxs-lookup"><span data-stu-id="32e74-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="32e74-512">Interface ILocaleString</span><span class="sxs-lookup"><span data-stu-id="32e74-512">ILocaleString interface</span></span>
<span data-ttu-id="32e74-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="32e74-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span></span>

<span data-ttu-id="32e74-514">A **ILocaleString** é uma estrutura de cadeia de caracteres localizada que contém uma cadeia de caracteres localizada e a identificação de localidade da localização.</span><span class="sxs-lookup"><span data-stu-id="32e74-514">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="32e74-515">A interface **ILocaleString** é usada para formatar a cadeia de caracteres de status personalizada no cartão de visita.</span><span class="sxs-lookup"><span data-stu-id="32e74-515">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="32e74-516">A Tabela 12 mostra os membros que devem ser implementados nas classes que são herdadas de **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="32e74-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="32e74-517">Qualquer membro da interface **ILocaleString** não listado na tabela deve estar presente, mas não precisa ser implementado.</span><span class="sxs-lookup"><span data-stu-id="32e74-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="32e74-518">Os membros que estão presentes, mas não implementados, podem gerar um erro **NotImplementedException** ou **E_NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="32e74-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="32e74-519">Para saber mais sobre a interface **ILocalString** e seus membros, confira [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="32e74-519">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](https://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="32e74-520">**Tabela 12. Implementação da interface ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="32e74-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="32e74-521">**Membro**</span><span class="sxs-lookup"><span data-stu-id="32e74-521">**Member**</span></span>|<span data-ttu-id="32e74-522">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="32e74-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32e74-523">Propriedade **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="32e74-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="32e74-524">Obtém a identificação de localidade.</span><span class="sxs-lookup"><span data-stu-id="32e74-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="32e74-525">Propriedade **Value**</span><span class="sxs-lookup"><span data-stu-id="32e74-525">**Value** property</span></span>  <br/> |<span data-ttu-id="32e74-526">Obtém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32e74-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32e74-527">Confira também</span><span class="sxs-lookup"><span data-stu-id="32e74-527">See also</span></span>

- <span data-ttu-id="32e74-528">Namespace [UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="32e74-528">[UCCollaborationLib](https://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

