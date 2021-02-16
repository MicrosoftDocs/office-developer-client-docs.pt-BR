---
title: Exemplo de provedor de transporte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356585"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="b3a1e-103">Exemplo de provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="b3a1e-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="b3a1e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3a1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3a1e-105">Este exemplo usa arquivos e diretórios para transmitir e receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="b3a1e-106">Ele implementa e registra um pré-processador muito simples que anexa uma linha de texto a cada mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="b3a1e-107">O exemplo ilustra como dividir o conteúdo da mensagem entre o TNEF (Transport Neutral Encapsulation Format) e o texto.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="b3a1e-108">Ele também oferece suporte a todas as opções de configuração (folhas de propriedades, assistentes e configuração programática) e opções de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="b3a1e-109">Ele não dá suporte às interfaces de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="b3a1e-110">Você pode baixar este exemplo dos exemplos de código [da API de Mensagens do Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3a1e-111">Executável:</span><span class="sxs-lookup"><span data-stu-id="b3a1e-111">Executable:</span></span>  <br/> |<span data-ttu-id="b3a1e-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="b3a1e-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="b3a1e-113">Diretório do código-fonte:</span><span class="sxs-lookup"><span data-stu-id="b3a1e-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="b3a1e-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="b3a1e-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="b3a1e-115">Idioma:</span><span class="sxs-lookup"><span data-stu-id="b3a1e-115">Language:</span></span>  <br/> |<span data-ttu-id="b3a1e-116">C++</span><span class="sxs-lookup"><span data-stu-id="b3a1e-116">C++</span></span>  <br/> |
|<span data-ttu-id="b3a1e-117">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="b3a1e-117">Platforms:</span></span>  <br/> |<span data-ttu-id="b3a1e-118">Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="b3a1e-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="b3a1e-119">Recursos com suporte</span><span class="sxs-lookup"><span data-stu-id="b3a1e-119">Supported Features</span></span>

<span data-ttu-id="b3a1e-120">Este exemplo dá suporte aos seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="b3a1e-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="b3a1e-121">Recursos básicos, como envio, recebimento e sondagem de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="b3a1e-122">Configuração interativa e programática.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="b3a1e-123">A interface **IMAPIStatus,** exceto para a configuração da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="b3a1e-124">Para obter mais informações, consulte a interface [IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="b3a1e-125">Segurança do thread.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-125">Thread safety.</span></span>
    
- <span data-ttu-id="b3a1e-126">Log de eventos para um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-126">Event logging to a text file.</span></span> <span data-ttu-id="b3a1e-127">O arquivo é automaticamente limitado a um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="b3a1e-128">Todas as sessões de transporte usam o mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="b3a1e-129">Recursos sem suporte</span><span class="sxs-lookup"><span data-stu-id="b3a1e-129">Unsupported Features</span></span>

<span data-ttu-id="b3a1e-130">Este exemplo não dá suporte à detecção assíncrona de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="b3a1e-131">**Para instalar o Provedor de Transporte de Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="b3a1e-132">Para baixar o Provedor de Transporte de Exemplo, consulte [Baixando os exemplos de MAPI do Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="b3a1e-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="b3a1e-133">Localize a pasta onde você salvou os exemplos de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="b3a1e-134">Clique com o botão direito do mouse na pasta zip do número de versão do **OutlookMAPISamples \< \>** e clique em **Extrair Tudo.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="b3a1e-135">Clique **em** Procurar, selecione o local onde deseja salvar o exemplo e clique em **Extrair.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="b3a1e-136">Execute o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="b3a1e-137">No Visual Studio 2008, clique em **Arquivo,** selecione **Abrir** e clique em **Projeto/Solução.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="b3a1e-138">Navegue até o local onde você salvou o exemplo, clique em **mrxp32.vcproj** e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="b3a1e-139">No menu **Criar,** clique em **Configuration Manager.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="b3a1e-140">Na caixa de **diálogo Configuration Manager,** vá para a linha  **mrxp32** e, na coluna Configuração, selecione **Liberar** e clique em **Fechar.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="b3a1e-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="b3a1e-142">Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="b3a1e-143">Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo de lote de instalação e clique em **Executar como administrador.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="b3a1e-144">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b3a1e-145">**install.bat** copia a .dll para a pasta de instalação padrão do Microsoft Office, C:\Arquivos de Programas\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="b3a1e-146">Se você instalou produtos do Office em um local diferente, clique com o botão direito do mouse **install.bat** e clique em **Editar.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="b3a1e-147">O arquivo é aberto no Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-147">The file opens in Notepad.</span></span> <span data-ttu-id="b3a1e-148">Substitua o caminho de instalação padrão pelo caminho de instalação usado no computador.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="b3a1e-149">**Para configurar o Provedor de Transporte no Outlook**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="b3a1e-150">No menu **Ferramentas** do Outlook, clique em **Configurações da Conta.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="b3a1e-151">Na caixa **de diálogo Configurações da** Conta, na guia **Email,** clique em **Novo.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="b3a1e-152">Em **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="b3a1e-153">Na caixa de diálogo Configuração de **Transporte MRXP,** digite um **Nome de Exibição do Usuário.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="b3a1e-154">Em **Caminho para Caixa de Entrada (Compartilhamento UNC),** insira um caminho de pasta.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="b3a1e-155">Isso também pode ser um caminho para uma pasta local.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="b3a1e-156">Esse caminho deve existir.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="b3a1e-157">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="b3a1e-158">Na caixa **de diálogo Adicionar Conta de Email,** clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="b3a1e-159">Clique **em Concluir** e em **Fechar.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="b3a1e-160">Para começar a usar a conta MRXP, saia e reinicie o Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="b3a1e-161">**Para usar o exemplo de provedor de transporte para enviar uma mensagem no Outlook**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="b3a1e-162">No menu **Arquivo,** clique em **Novo** e em Mensagem **de Email.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b3a1e-163">Na caixa **Para,** digite o nome do destinatário usando o **formato [MRXP: \< ENDEREÇO \> ]**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="b3a1e-164">O endereço é o compartilhamento UNC ou o caminho da pasta local para a caixa de entrada do destinatário.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b3a1e-165">Se houver dois-pontos ou uma malha invertida no endereço, você deve inserir uma faixa invertida antes de cada dois-pontos ou uma faixa invertida.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="b3a1e-166">Por exemplo, para enviar emails para [MRXP:C:\Mail\myDir] você deve digitar  `[MRXP:C\:\\Mail\\myDir]` .</span><span class="sxs-lookup"><span data-stu-id="b3a1e-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="b3a1e-167">O endereço do destinatário deve existir.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="b3a1e-168">Clique **em Conta** e em Transporte de Exemplo **MRXP.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="b3a1e-169">Digite sua mensagem e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-169">Type your message and click **Send**.</span></span> <span data-ttu-id="b3a1e-170">A mensagem é enviada usando o provedor de transporte MRXP.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="b3a1e-171">**Para usar o exemplo de provedor de transporte para receber uma mensagem no Outlook**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="b3a1e-172">No menu **Arquivo,** clique em **Novo** e em Mensagem **de Email.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b3a1e-173">Digite sua mensagem.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-173">Type your message.</span></span>
    
3. <span data-ttu-id="b3a1e-174">Clique no **Botão do Microsoft Office,**  clique em Salvar **como** e, em seguida, clique em Salvar como para salvar o arquivo na pasta da caixa de entrada especificada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="b3a1e-175">Na caixa **de diálogo Salvar como,** navegue até o compartilhamento UNC ou pasta local que você definiu como sua caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="b3a1e-176">No drop **down Salvar como tipo,** clique em **Formato de Mensagem do Outlook.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="b3a1e-177">Digite um nome para o arquivo e clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="b3a1e-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="b3a1e-178">O arquivo é salvo na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="b3a1e-179">O provedor de transporte MRXP entrega a mensagem à sua Caixa de Entrada no Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3a1e-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

