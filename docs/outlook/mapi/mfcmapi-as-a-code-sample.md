---
title: MFCMAPI como exemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356858"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="e4973-103">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e4973-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="e4973-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4973-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4973-105">O exemplo MFCMAPI usa a API de Mensagens para fornecer acesso a armazenamentos MAPI por meio de uma interface gráfica do usuário.</span><span class="sxs-lookup"><span data-stu-id="e4973-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="e4973-106">Depois de baixar esse exemplo, você pode usar os arquivos de origem para examinar exemplos de casos de uso de muitas das interfaces e referências MAPI.</span><span class="sxs-lookup"><span data-stu-id="e4973-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="e4973-107">Para obter mais informações, consulte [Interfaces MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e4973-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4973-108">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="e4973-108">Platforms:</span></span>  <br/> |<span data-ttu-id="e4973-109">Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="e4973-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="e4973-110">Para baixar MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e4973-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="e4973-111">Na página [MFCMAPI,](https://codeplex.com/MFCMAPI) clique na guia **Código-fonte.**</span><span class="sxs-lookup"><span data-stu-id="e4973-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="e4973-112">Em **Check-Ins Recentes,** clique **em Baixar** para a com build mais recente.</span><span class="sxs-lookup"><span data-stu-id="e4973-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="e4973-113">Leia o contrato de licença e clique em **Concordar.**</span><span class="sxs-lookup"><span data-stu-id="e4973-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="e4973-114">Na caixa de diálogo **Download de Arquivo**, clique em **Salvar**.</span><span class="sxs-lookup"><span data-stu-id="e4973-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="e4973-115">Na caixa **de diálogo Salvar como,** localize a pasta na qual você deseja salvar os arquivos de origem e clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="e4973-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="e4973-116">Na caixa **de diálogo Baixar Concluído,** clique em **Abrir Pasta.**</span><span class="sxs-lookup"><span data-stu-id="e4973-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="e4973-117">Você também pode clicar **em Fechar** para fechar a caixa de diálogo e localizar os arquivos de origem recortados na pasta em que os salvou.</span><span class="sxs-lookup"><span data-stu-id="e4973-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="e4973-118">Clique com o botão direito do mouse no arquivo .zip do número de versão **\< \> MFCMAPI** e clique em **Extrair Tudo.**</span><span class="sxs-lookup"><span data-stu-id="e4973-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="e4973-119">Na caixa de diálogo exibida, clique em **Extrair** para extrair os arquivos para a pasta exibida.</span><span class="sxs-lookup"><span data-stu-id="e4973-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="e4973-120">Você também pode clicar **em Procurar** para selecionar ou criar uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="e4973-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="e4973-121">Execute o Visual Studio 2008 como administrador.</span><span class="sxs-lookup"><span data-stu-id="e4973-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="e4973-122">Se o computador estiver executando o Windows XP, você deverá estar conectado como administrador.</span><span class="sxs-lookup"><span data-stu-id="e4973-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="e4973-123">Se o computador estiver executando o Windows Vista, você deverá estar conectado como administrador e clicar com o botão direito do mouse no ícone do Visual Studio 2008 e clicar em Executar **como administrador.**</span><span class="sxs-lookup"><span data-stu-id="e4973-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="e4973-124">No Visual Studio 2008, clique em **Arquivo,** aponte para **Abrir** e clique em **Projeto/Solução.**</span><span class="sxs-lookup"><span data-stu-id="e4973-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="e4973-125">Navegue até o local onde você salvou o exemplo, selecione **MFCMapi.vcproj** e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="e4973-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="e4973-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="e4973-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="e4973-127">Na caixa **de diálogo Salvar Arquivo como,** clique em **Salvar.**</span><span class="sxs-lookup"><span data-stu-id="e4973-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="e4973-128">Para usar MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e4973-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="e4973-129">No **Solution Explorer,** expanda o projeto **MFCMapi** e examine os arquivos nos nós Arquivos de **Header**, **Arquivos** de Recurso e Arquivos **de** Origem para cenários de programação.</span><span class="sxs-lookup"><span data-stu-id="e4973-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="e4973-130">Muitos tópicos de método na seção [Interfaces MAPI](mapi-interfaces.md) apontam para arquivos de origem MFCMAPI para exemplos de programação.</span><span class="sxs-lookup"><span data-stu-id="e4973-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="e4973-131">Por exemplo, em [IMsgStore::GetReceiveFolderTable,](imsgstore-getreceivefoldertable.md) você é instruído a olhar para a função no  `CMsgStoreDlg::OnDisplayReceiveFolderTable` arquivo MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="e4973-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4973-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4973-132">See also</span></span>

- [<span data-ttu-id="e4973-133">Amostras MAPI</span><span class="sxs-lookup"><span data-stu-id="e4973-133">MAPI Samples</span></span>](mapi-samples.md)

