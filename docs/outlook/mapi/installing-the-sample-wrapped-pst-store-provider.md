---
title: Instalando o provedor de repositório PST encapsulado de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309629"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b6f89-103">Instalando o provedor de repositório PST encapsulado de exemplo</span><span class="sxs-lookup"><span data-stu-id="b6f89-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="b6f89-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6f89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6f89-105">Este tópico orienta as etapas para baixar e instalar o exemplo de provedor de repositório PST encapsulado.</span><span class="sxs-lookup"><span data-stu-id="b6f89-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="b6f89-106">O exemplo de provedor de repositório PST encapsulado, WrapPST, implementa um provedor de repositório PST encapsulado que deve ser usado em conjunto com a API de replicação.</span><span class="sxs-lookup"><span data-stu-id="b6f89-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="b6f89-107">Para obter mais informações sobre a API de replicação, consulte [About The Replication API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="b6f89-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="b6f89-108">Instalar o exemplo de provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="b6f89-109">Para baixar o exemplo de provedor de repositório PST encapsulado, confira [exemplos de código de referência auxiliar do Outlook 2007 e instalador](https://www.microsoft.com/en-us/download/details.aspx?id=24102)redistribuível.</span><span class="sxs-lookup"><span data-stu-id="b6f89-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="b6f89-110">Abra a pasta **SampleWrappedPSTStoreProvider** e clique em **extrair todos os arquivos**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="b6f89-111">Clique em **procurar**, selecione o local onde deseja salvar o exemplo e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="b6f89-112">Clique em **Extrair**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-112">Click **Extract**.</span></span> <span data-ttu-id="b6f89-113">A pasta selecionada aparece e contém os arquivos extraídos.</span><span class="sxs-lookup"><span data-stu-id="b6f89-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="b6f89-114">Abra o Visual Studio 2005 como um administrador.</span><span class="sxs-lookup"><span data-stu-id="b6f89-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b6f89-115">Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador.</span><span class="sxs-lookup"><span data-stu-id="b6f89-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="b6f89-116">Se seu computador está executando o Windows Vista, você deve estar conectado como administrador e deve clicar com o botão direito do mouse no ícone do Visual Studio 2005 e clicar em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="b6f89-117">No Visual Studio 2005, clique em **arquivo**, selecione **abrir**e, em seguida, clique em **projeto/solução**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="b6f89-118">Navegue até o local onde você salvou o exemplo, clique em **WrapPST**e, em seguida, clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="b6f89-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="b6f89-120">Na caixa de diálogo **salvar arquivo como** , clique em **salvar**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="b6f89-121">Na pasta onde você salvou o exemplo, clique com o botão direito do mouse no arquivo **install. bat** e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="b6f89-122">Na caixa de diálogo **Controle de Conta de Usuário**, clique em **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="b6f89-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6f89-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6f89-123">See also</span></span>



[<span data-ttu-id="b6f89-124">Sobre o exemplo de provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b6f89-125">Inicializando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b6f89-126">Fazer logon em um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b6f89-127">Usando um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="b6f89-128">DesLigamento de um provedor de repositório PST encapsulado</span><span class="sxs-lookup"><span data-stu-id="b6f89-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

