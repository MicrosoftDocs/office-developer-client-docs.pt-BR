---
title: Instalar o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 7616c3a6077b9354cda7046c0949e7c5553f6551
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586834"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="acb81-103">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="acb81-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acb81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acb81-105">Este tópico leva as etapas para baixar e instalar o suplemento de amostra Offline estado.</span><span class="sxs-lookup"><span data-stu-id="acb81-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="acb81-106">O suplemento de amostra Offline estado é um suplemento de COM que adiciona um menu de **Estado Offline** para o Outlook e utiliza a API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="acb81-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="acb81-107">Através do menu estado Offline, você pode habilitar ou desabilitar o monitoramento do estado, verifique o estado atual e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="acb81-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="acb81-108">Para obter mais informações sobre como o suplemento de estado Offline é implementado, consulte [Add-in de configuração para cima uma Offline estado](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="acb81-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="acb81-109">Instalar o amostra Offline State suplemento</span><span class="sxs-lookup"><span data-stu-id="acb81-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="acb81-110">Baixar o Add-in amostra Offline estado aqui: [amostras de código de referência de auxiliar do Outlook 2007 e instalador redistribuível](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="acb81-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="acb81-111">Execute o Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="acb81-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="acb81-112">Se seu computador estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="acb81-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="acb81-113">Se seu computador estiver executando o Windows Vista, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="acb81-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="acb81-114">Com o botão direito no ícone do Visual Studio 2005 e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="acb81-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="acb81-115">No Visual Studio 2005, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="acb81-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="acb81-116">Navegue até o local onde você salvou a amostra, clique em **ConnectionStateAddin**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="acb81-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="acb81-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="acb81-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="acb81-118">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="acb81-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="acb81-119">Clique no menu **Iniciar** , clique em **Todos os programas**, clique em **Acessórios**, do mouse em **Prompt de comando**e, em seguida, clique **em Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="acb81-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="acb81-120">Se você estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="acb81-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="acb81-121">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="acb81-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="acb81-122">Na janela de **Prompt de comando** , altere os diretórios para a pasta de depuração onde você salvou a amostra.</span><span class="sxs-lookup"><span data-stu-id="acb81-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="acb81-123">Por exemplo, se você salvou a amostra em sua unidade C:\, digite **cd "C:\ConnectionStateAddin\Debug"** e pressione **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="acb81-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="acb81-124">Digite **regsvr32 OfflineStateAddin.dll** e pressione **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="acb81-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="acb81-125">Para desinstalar o suplemento de amostra Offline estado, digite **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="acb81-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="acb81-126">Na caixa de diálogo **regsvr32** , clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="acb81-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="acb81-127">Reinicie o Outlook para ver o menu de **Estado Offline** .</span><span class="sxs-lookup"><span data-stu-id="acb81-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="acb81-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb81-128">See also</span></span>



[<span data-ttu-id="acb81-129">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="acb81-130">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="acb81-131">Sobre o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="acb81-132">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="acb81-133">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="acb81-134">Desconectar-se de um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="acb81-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

