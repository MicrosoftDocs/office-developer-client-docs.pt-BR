---
title: Instalar o exemplo de suplemento de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Última modificação: 06 de julho de 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317210"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="d67e2-103">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="d67e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d67e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d67e2-105">Este tópico orienta as etapas para baixar e instalar o exemplo de suplemento de estado offline.</span><span class="sxs-lookup"><span data-stu-id="d67e2-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="d67e2-106">O exemplo de suplemento de estado offline é um suplemento de COM que adiciona um menu de **estado offline** ao Outlook e utiliza a API de estado offline.</span><span class="sxs-lookup"><span data-stu-id="d67e2-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="d67e2-107">No menu de estado offline, você pode habilitar ou desabilitar o monitoramento de estado, verificar o estado atual e alterar o estado atual.</span><span class="sxs-lookup"><span data-stu-id="d67e2-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="d67e2-108">Para obter mais informações sobre como o suplemento de estado offline é implementado, consulte [Configurando um suplemento de estado offline](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="d67e2-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="d67e2-109">Instalar o exemplo de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="d67e2-110">Baixe o exemplo de suplemento offline State aqui: [exemplos de código de referência auxiliar do Outlook 2007 e instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuível.</span><span class="sxs-lookup"><span data-stu-id="d67e2-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="d67e2-111">Execute o Visual Studio 2005 como um administrador.</span><span class="sxs-lookup"><span data-stu-id="d67e2-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d67e2-112">Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador.</span><span class="sxs-lookup"><span data-stu-id="d67e2-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="d67e2-113">Se o computador estiver executando o Windows Vista, você deverá estar conectado como administrador.</span><span class="sxs-lookup"><span data-stu-id="d67e2-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="d67e2-114">Clique com o botão direito do mouse no ícone do Visual Studio 2005 e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="d67e2-115">No Visual Studio 2005, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="d67e2-116">Navegue até o local onde você salvou o exemplo, clique em **ConnectionStateAddin**e, em seguida, clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="d67e2-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="d67e2-118">Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="d67e2-119">Clique no menu **Iniciar** , em **todos os programas**, em **acessórios**, clique com o botão direito do mouse em prompt de **comando**e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d67e2-120">Se você estiver executando o Windows XP, você deve estar conectado como um administrador.</span><span class="sxs-lookup"><span data-stu-id="d67e2-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="d67e2-121">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="d67e2-122">Na janela de **prompt de comando** , altere os diretórios para a pasta de depuração onde você salvou o exemplo.</span><span class="sxs-lookup"><span data-stu-id="d67e2-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="d67e2-123">Por exemplo, se você salvou o exemplo em C:\ Digite **CD "C:\ConnectionStateAddin\Debug"** e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="d67e2-124">Digite **regsvr32 OfflineStateAddin. dll** e pressione **Enter**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="d67e2-125">Para desinstalar o exemplo de suplemento de estado offline, digite **regsvr32-u OfflineStateAddin. dll**</span><span class="sxs-lookup"><span data-stu-id="d67e2-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="d67e2-126">Na caixa de diálogo **RegSrv32** , clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d67e2-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="d67e2-127">ReInicie o Outlook para ver o menu de **estado offline** .</span><span class="sxs-lookup"><span data-stu-id="d67e2-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d67e2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d67e2-128">See also</span></span>



[<span data-ttu-id="d67e2-129">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="d67e2-130">Instalar a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="d67e2-131">Sobre a amostra de suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="d67e2-132">Configurar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="d67e2-133">Monitorar alterações de estado da conexão usando um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="d67e2-134">Desconectar um suplemento de estado offline</span><span class="sxs-lookup"><span data-stu-id="d67e2-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

