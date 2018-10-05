---
title: MFCMAPI como um exemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391653"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="efeb7-103">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="efeb7-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="efeb7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efeb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efeb7-105">O exemplo MFCMAPI usa a API do serviço de mensagens para fornecer acesso a repositórios MAPI através de uma interface gráfica do usuário.</span><span class="sxs-lookup"><span data-stu-id="efeb7-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="efeb7-106">Após você baixa esse exemplo, você pode usar os arquivos de origem para examinar os casos de uso de exemplo para muitas das interfaces MAPI e referências.</span><span class="sxs-lookup"><span data-stu-id="efeb7-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="efeb7-107">Para obter mais informações, consulte [Interfaces de MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="efeb7-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efeb7-108">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="efeb7-108">Platforms:</span></span>  <br/> |<span data-ttu-id="efeb7-109">Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="efeb7-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="efeb7-110">Para baixar MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="efeb7-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="efeb7-111">Na página [MFCMAPI](https://codeplex.com/MFCMAPI) , clique na guia do **Código-fonte** .</span><span class="sxs-lookup"><span data-stu-id="efeb7-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="efeb7-112">Em **Recentes Check-Ins**, clique em **Download** para a compilação mais recente.</span><span class="sxs-lookup"><span data-stu-id="efeb7-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="efeb7-113">Leia o contrato de licença e clique em **concordo**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="efeb7-114">Na caixa de diálogo **Download de arquivo** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="efeb7-115">Na caixa de diálogo **Salvar como** , localize a pasta na qual deseja salvar os arquivos de origem e, em seguida, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="efeb7-116">Na caixa de diálogo **Download concluído** , clique em **Abrir pasta**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="efeb7-117">Também é possível clicar **Fechar** para fechar a caixa de diálogo e localize os arquivos de origem compactados na pasta que você salvou-los na.</span><span class="sxs-lookup"><span data-stu-id="efeb7-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="efeb7-118">Com o botão direito do **MFCMAPI -\<número da versão\>. zip** de arquivo e clique em **Extrair todos**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="efeb7-119">Na caixa de diálogo que aparece, clique em **extrair** para extrair os arquivos para a pasta que é exibida.</span><span class="sxs-lookup"><span data-stu-id="efeb7-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="efeb7-120">Você também pode clicar em **Procurar** para selecionar ou criar uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="efeb7-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="efeb7-121">Execute o Visual Studio 2008 como administrador.</span><span class="sxs-lookup"><span data-stu-id="efeb7-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="efeb7-122">Se seu computador estiver executando o Windows XP, você deve ser logado como administrador.</span><span class="sxs-lookup"><span data-stu-id="efeb7-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="efeb7-123">Se seu computador estiver executando o Windows Vista, você deve estar logado como administrador e você deve com o botão direito no ícone do Visual Studio 2008 e clique em **Executar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="efeb7-124">No Visual Studio 2008, clique em **arquivo**, aponte para **Abrir**e, em seguida, clique em **Project/Solution**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="efeb7-125">Navegue até o local onde você salvou a amostra, selecione **MFCMapi.vcproj**e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="efeb7-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="efeb7-127">Na caixa de diálogo **Salvar arquivo como** , clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="efeb7-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="efeb7-128">Para usar MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="efeb7-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="efeb7-129">No **Solution Explorer**, expanda o projeto **MFCMapi** e examinar os arquivos nos nós de **Arquivos de cabeçalho**, **Arquivos de recursos**e **Arquivos de origem** para cenários de programação.</span><span class="sxs-lookup"><span data-stu-id="efeb7-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="efeb7-130">Muitos tópicos do método na seção de [Interfaces de MAPI](mapi-interfaces.md) apontam para os arquivos de origem MFCMAPI para obter exemplos de programação.</span><span class="sxs-lookup"><span data-stu-id="efeb7-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="efeb7-131">Por exemplo, no [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) instruído para examinar a função `CMsgStoreDlg::OnDisplayReceiveFolderTable` no arquivo MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="efeb7-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efeb7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="efeb7-132">See also</span></span>

- [<span data-ttu-id="efeb7-133">Amostras MAPI</span><span class="sxs-lookup"><span data-stu-id="efeb7-133">MAPI Samples</span></span>](mapi-samples.md)

