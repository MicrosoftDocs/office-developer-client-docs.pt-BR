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
ms.openlocfilehash: 1d0538f02f852580c064560460bb8b2ba54a2f65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770661"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="6e1c2-103">Exemplo de provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="6e1c2-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="6e1c2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e1c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e1c2-105">Este exemplo usa os arquivos e diretórios para transmitir e receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="6e1c2-106">Ela implementa e registra um pré-processador muito simple que acrescenta uma linha de texto a cada mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="6e1c2-107">O exemplo ilustra como dividir o conteúdo da mensagem entre TNEF Transport Neutral Encapsulation Format () e o texto.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="6e1c2-108">Ele também oferece suporte a todas as opções de configuração (folhas de propriedades, assistentes e configuração programática) e opções de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="6e1c2-109">Ele não suporta as interfaces de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="6e1c2-110">Você pode baixar esse exemplo de [Amostras de código do Outlook Messaging API (MAPI)](http://go.microsoft.com/fwlink/?LinkId=129740).</span><span class="sxs-lookup"><span data-stu-id="6e1c2-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](http://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e1c2-111">Executável:</span><span class="sxs-lookup"><span data-stu-id="6e1c2-111">Executable:</span></span>  <br/> |<span data-ttu-id="6e1c2-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="6e1c2-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="6e1c2-113">Diretório de origem do código:</span><span class="sxs-lookup"><span data-stu-id="6e1c2-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="6e1c2-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="6e1c2-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="6e1c2-115">Idioma:</span><span class="sxs-lookup"><span data-stu-id="6e1c2-115">Language:</span></span>  <br/> |<span data-ttu-id="6e1c2-116">C++</span><span class="sxs-lookup"><span data-stu-id="6e1c2-116">C++</span></span>  <br/> |
|<span data-ttu-id="6e1c2-117">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="6e1c2-117">Platforms:</span></span>  <br/> |<span data-ttu-id="6e1c2-118">Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="6e1c2-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="6e1c2-119">Recursos compatíveis</span><span class="sxs-lookup"><span data-stu-id="6e1c2-119">Supported Features</span></span>

<span data-ttu-id="6e1c2-120">Este exemplo aceita os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="6e1c2-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="6e1c2-121">Recursos básicos como enviar, receber e sondagem de novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="6e1c2-122">Configuração interativa e programática.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="6e1c2-123">A interface **IMAPIStatus** , exceto para a configuração da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="6e1c2-124">Para obter mais informações, consulte o [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="6e1c2-125">Acesso thread-safe.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-125">Thread safety.</span></span>
    
- <span data-ttu-id="6e1c2-126">Log de eventos para um arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-126">Event logging to a text file.</span></span> <span data-ttu-id="6e1c2-127">O arquivo está limitado automaticamente em um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="6e1c2-128">Todas as sessões de transporte usam o mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="6e1c2-129">Recursos sem suporte</span><span class="sxs-lookup"><span data-stu-id="6e1c2-129">Unsupported Features</span></span>

<span data-ttu-id="6e1c2-130">Este exemplo não oferece suporte a detecção assíncrona de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="6e1c2-131">**Para instalar o provedor de transporte de amostra**</span><span class="sxs-lookup"><span data-stu-id="6e1c2-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="6e1c2-132">Para baixar o provedor de transporte de amostra, consulte [Baixando as amostras de MAPI do Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="6e1c2-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="6e1c2-133">Localize a pasta onde você salvou as amostras de MAPI do Outlook.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="6e1c2-134">Com o botão direito do **OutlookMAPISamples -\<o número de versão\> ** zip pasta e clique em **Extrair tudo**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="6e1c2-135">Clique em **Procurar**, selecione o local onde deseja salvar a amostra e clique em **extrair**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="6e1c2-136">Execute o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="6e1c2-137">No Visual Studio 2008, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="6e1c2-138">Navegue até o local onde você salvou a amostra, clique em **mrxp32.vcproj**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="6e1c2-139">No menu **Build** , clique em **Gerenciador de configuração**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="6e1c2-140">Na caixa de diálogo **Gerenciador de configuração** , vá para a linha de **mrxp32** , na coluna **configuração** , selecione **versão**e, em seguida, clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="6e1c2-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="6e1c2-142">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="6e1c2-143">Na pasta onde você salvou a amostra, clique com o botão o arquivo de lote de instalação e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="6e1c2-144">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e1c2-145">**Install. bat** copia o arquivo. dll na pasta de instalação do Microsoft Office padrão, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="6e1c2-146">Se você tiver instalado os produtos do Office em um local diferente, clique com o botão **Install. bat** e clique em **Editar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="6e1c2-147">O arquivo será aberto no bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-147">The file opens in Notepad.</span></span> <span data-ttu-id="6e1c2-148">Substitua o caminho de instalação padrão do caminho de instalação usado no seu computador.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="6e1c2-149">**Para configurar o provedor de transporte no Outlook**</span><span class="sxs-lookup"><span data-stu-id="6e1c2-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="6e1c2-150">No menu **Ferramentas** do Outlook, clique em **Configurações de conta**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="6e1c2-151">Na caixa de diálogo **Configurações de conta** , na guia **Email** , clique em **novo**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="6e1c2-152">Em **Escolher serviço de Email** clique em **outros**, selecione **Transporte de amostra MRXP**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="6e1c2-153">Na caixa de diálogo **Configuração de transporte MRXP** digite um **Nome de exibição do usuário**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="6e1c2-154">Em **caminho para a caixa de entrada (compartilhamento UNC)** Insira um caminho de pasta.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="6e1c2-155">Isso também pode ser um caminho para uma pasta local.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6e1c2-156">Esse caminho deve existir.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="6e1c2-157">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="6e1c2-158">Na caixa de diálogo **Adicionar conta de Email** , clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="6e1c2-159">Clique em **Concluir** e clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="6e1c2-160">Para começar a usar a conta MRXP, saia e reinicie o Outlook.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="6e1c2-161">**Usar o exemplo de provedor de transporte para enviar uma mensagem no Outlook**</span><span class="sxs-lookup"><span data-stu-id="6e1c2-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="6e1c2-162">No menu **arquivo** , clique em **novo**e, em seguida, clique em **Email**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="6e1c2-163">Na caixa **para** , digite o nome do destinatário usando o formato **[MRXP:\<endereço\>]**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="6e1c2-164">O endereço é o compartilhamento UNC ou o caminho da pasta local na caixa de entrada do destinatário.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e1c2-165">Se houver dois pontos ou barras invertidas no endereço, você deve inserir uma barra invertida antes de cada dois-pontos ou barra invertida.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="6e1c2-166">Por exemplo, para enviar email para [MRXP:C:\Mail\myDir] deverá digitar `[MRXP:C\:\\Mail\\myDir]`.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="6e1c2-167">O endereço do destinatário deve existir.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="6e1c2-168">Clique na **conta** e clique em **MRXP amostra transporte**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="6e1c2-169">Digite sua mensagem e clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-169">Type your message and click **Send**.</span></span> <span data-ttu-id="6e1c2-170">A mensagem é enviada usando o provedor de transporte MRXP.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="6e1c2-171">**Usar o exemplo de provedor de transporte para receber uma mensagem no Outlook**</span><span class="sxs-lookup"><span data-stu-id="6e1c2-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="6e1c2-172">No menu **arquivo** , clique em **novo**e, em seguida, clique em **Email**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="6e1c2-173">Digite sua mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-173">Type your message.</span></span>
    
3. <span data-ttu-id="6e1c2-174">Clique no **Botão do Microsoft Office**, clique em **Salvar como**e, em seguida, clique em **Salvar como** para salvar o arquivo para a pasta de entrada especificada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="6e1c2-175">Na caixa de diálogo **Salvar como** , navegue até o compartilhamento UNC ou uma pasta local que você definiu como sua caixa de entrada.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="6e1c2-176">Na lista suspensa **Salvar como tipo** , clique em **Formato de mensagem do Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="6e1c2-177">Digite um nome para o arquivo e clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="6e1c2-178">O arquivo é salvo na pasta compartilhada.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="6e1c2-179">O provedor de transporte MRXP entrega a mensagem para sua caixa de entrada no Outlook.</span><span class="sxs-lookup"><span data-stu-id="6e1c2-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

