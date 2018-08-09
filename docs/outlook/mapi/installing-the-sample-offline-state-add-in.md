---
title: Instalar o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Modificado pela última vez: 06 de julho de 2012'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767584"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="9bb87-103">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="9bb87-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bb87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bb87-105">Este tópico leva as etapas para baixar e instalar o suplemento de amostra Offline estado.</span><span class="sxs-lookup"><span data-stu-id="9bb87-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="9bb87-106">O suplemento de amostra Offline estado é um suplemento de COM que adiciona um menu de **Estado Offline** para o Outlook e utiliza a API de estado Offline.</span><span class="sxs-lookup"><span data-stu-id="9bb87-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="9bb87-107">Através do menu estado Offline, você pode habilitar ou desabilitar o monitoramento do estado, verifique o estado atual e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="9bb87-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="9bb87-108">Para obter mais informações sobre como o suplemento de estado Offline é implementado, consulte [Add-in de configuração para cima uma Offline estado](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="9bb87-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="9bb87-109">Instalar o amostra Offline State suplemento</span><span class="sxs-lookup"><span data-stu-id="9bb87-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="9bb87-110">Baixar o Add-in amostra Offline estado aqui: [amostras de código de referência de auxiliar do Outlook 2007 e instalador redistribuível](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="9bb87-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="9bb87-111">Execute o Visual Studio 2005 como administrador.</span><span class="sxs-lookup"><span data-stu-id="9bb87-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9bb87-112">Se seu computador estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="9bb87-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="9bb87-113">Se seu computador estiver executando o Windows Vista, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="9bb87-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="9bb87-114">Com o botão direito no ícone do Visual Studio 2005 e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="9bb87-115">No Visual Studio 2005, clique em **arquivo**, selecione **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="9bb87-116">Navegue até o local onde você salvou a amostra, clique em **ConnectionStateAddin**e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="9bb87-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="9bb87-118">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="9bb87-119">Clique no menu **Iniciar** , clique em **Todos os programas**, clique em **Acessórios**, do mouse em **Prompt de comando**e, em seguida, clique **em Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9bb87-120">Se você estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="9bb87-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="9bb87-121">Na caixa de diálogo **Controle de conta de usuário** , clique em **continuar**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="9bb87-122">Na janela de **Prompt de comando** , altere os diretórios para a pasta de depuração onde você salvou a amostra.</span><span class="sxs-lookup"><span data-stu-id="9bb87-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="9bb87-123">Por exemplo, se você salvou a amostra em sua unidade C:\, digite **cd "C:\ConnectionStateAddin\Debug"** e pressione **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="9bb87-124">Digite **regsvr32 OfflineStateAddin.dll** e pressione **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9bb87-125">Para desinstalar o suplemento de amostra Offline estado, digite **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="9bb87-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="9bb87-126">Na caixa de diálogo **regsvr32** , clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="9bb87-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="9bb87-127">Reinicie o Outlook para ver o menu de **Estado Offline** .</span><span class="sxs-lookup"><span data-stu-id="9bb87-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9bb87-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb87-128">See also</span></span>



[<span data-ttu-id="9bb87-129">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="9bb87-130">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="9bb87-131">Sobre o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="9bb87-132">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="9bb87-133">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="9bb87-134">Desconectar-se de um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="9bb87-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

