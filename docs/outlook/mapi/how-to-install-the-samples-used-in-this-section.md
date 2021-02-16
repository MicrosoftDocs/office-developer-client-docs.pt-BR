---
title: Instalar os exemplos usados nesta seção
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345546"
---
# <a name="install-the-samples-used-in-this-section"></a><span data-ttu-id="80988-103">Instalar os exemplos usados nesta seção</span><span class="sxs-lookup"><span data-stu-id="80988-103">Install the samples used in this section</span></span>

<span data-ttu-id="80988-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80988-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80988-105">Para instalar o aplicativo MFCMAPI e o projeto CreateOutlookItemsAddin para exibir e executar o código de exemplo referenciado pelos tópicos na seção Criando itens do Outlook usando [MAPI,](creating-outlook-items-by-using-mapi.md) siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="80988-105">To install the MFCMAPI application and CreateOutlookItemsAddin project to view and run the sample code referenced by the topics in the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section, follow these steps.</span></span> 

<span data-ttu-id="80988-106">Para baixar e instalar os exemplos usados na seção "Usando MAPI para criar itens do Outlook", siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="80988-106">To download and install the examples used in the "Using MAPI to create Outlook items" section, follow these steps.</span></span>

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a><span data-ttu-id="80988-107">Para baixar e instalar o aplicativo MFCMAPI e abrir o projeto CreateOutlookItemsAddin</span><span class="sxs-lookup"><span data-stu-id="80988-107">To download and install the MFCMAPI application and open CreateOutlookItemsAddin project</span></span>

1. <span data-ttu-id="80988-108">Baixe a versão atual do [executável MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) para uma pasta em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="80988-108">Download the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) executable to a folder on your system.</span></span> 
    
2. <span data-ttu-id="80988-109">Extraia MFCMapi.exe arquivo de MFCMapi.exe.</span><span class="sxs-lookup"><span data-stu-id="80988-109">Extract the MFCMapi.exe file in MFCMapi.exe.</span></span> <span data-ttu-id="80988-110">_version_.zip to an empty folder on your hard drive.</span><span class="sxs-lookup"><span data-stu-id="80988-110">_version_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="80988-111">Baixe a versão atual do [projeto CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828)</span><span class="sxs-lookup"><span data-stu-id="80988-111">Download the current version of the [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) project.</span></span> 
    
4. <span data-ttu-id="80988-112">Extraia todos os arquivos CreateOutlookItemsAddin.zip arquivo para a pasta onde você extraiu o arquivo MFCMapi.exe na Etapa 2.</span><span class="sxs-lookup"><span data-stu-id="80988-112">Extract all the files in the CreateOutlookItemsAddin.zip file to the folder where you extracted the MFCMapi.exe file in Step 2.</span></span>
    
5. <span data-ttu-id="80988-113">Copie MFCMapi.exe da pasta usada na Etapa 2 para o diretório de com build do projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).</span><span class="sxs-lookup"><span data-stu-id="80988-113">Copy MFCMapi.exe from the folder used in Step 2 to the build directory for the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\Debug).</span></span>
    
6. <span data-ttu-id="80988-114">Abra o projeto CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) no Visual Studio para examinar o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="80988-114">Open the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio to examine the source code.</span></span> <span data-ttu-id="80988-115">Consulte os tópicos da seção Criando itens do [Outlook usando MAPI](creating-outlook-items-by-using-mapi.md) para determinar quais arquivos de origem serão abertos.</span><span class="sxs-lookup"><span data-stu-id="80988-115">Refer to the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section to determine which source files to open.</span></span> 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a><span data-ttu-id="80988-116">Executar MFCMAPI e o projeto CreateOutlookItemsAddin</span><span class="sxs-lookup"><span data-stu-id="80988-116">Run MFCMAPI and the CreateOutlookItemsAddin project</span></span>

<span data-ttu-id="80988-117">As etapas a seguir presumem que você tenha baixado e instalado a versão atual do executável MFCMAPI e do projeto CreateOutlookItemsAddin conforme descrito no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="80988-117">The following steps assume that you have downloaded and installed the current version of the MFCMAPI executable and the CreateOutlookItemsAddin project as described in the preceding procedure.</span></span> <span data-ttu-id="80988-118">Estas etapas orientarão você para os itens de menu **Addins** que permitem criar itens do Outlook usando o aplicativo MFCMAPI e o projeto CreateOutlookItemsAddin.</span><span class="sxs-lookup"><span data-stu-id="80988-118">These steps will guide you to the **Addins** menu items that enable you to create Outlook items using the MFCMAPI application and the CreateOutlookItemsAddin project.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="80988-119">A pasta selecionada na etapa 8 e o comando selecionado na etapa 9 dependem do tipo de item discutido em um dos tópicos da seção Criando itens do Outlook usando [MAPI.](creating-outlook-items-by-using-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="80988-119">The folder you select in step 8, and the command you select in step 9, depends on the item type discussed in one of the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section.</span></span> 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a><span data-ttu-id="80988-120">Para executar os comandos do aplicativo MFCMAPI e do menu Addins</span><span class="sxs-lookup"><span data-stu-id="80988-120">To run the MFCMAPI application and Addins menu commands</span></span>

1. <span data-ttu-id="80988-121">Inicie Mfcmapi.exe na pasta CreateOutlookItemsAddin\Debug que é criada quando você segue as instruções de instalação.</span><span class="sxs-lookup"><span data-stu-id="80988-121">Start Mfcmapi.exe in the CreateOutlookItemsAddin\Debug folder that is created when you follow the installation instructions.</span></span>
    
2. <span data-ttu-id="80988-122">Clique **em OK** para descartar a tela inicial MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="80988-122">Click **OK** to dismiss the MFCMAPI splash screen.</span></span> 
    
3. <span data-ttu-id="80988-123">No menu **Sessão,** clique em **Logon e Exibir Tabela do Store.**</span><span class="sxs-lookup"><span data-stu-id="80988-123">On the **Session** menu, click **Logon and Display Store Table**.</span></span>
    
4. <span data-ttu-id="80988-124">Na caixa **de diálogo Escolher** Perfil, selecione o perfil correto e clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="80988-124">In the **Choose Profile** dialog box, select the correct profile, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="80988-125">Clique duas vezes **em Caixa de Correio – _[Nome de Usuário]_** na exibição de lista da tabela da loja.</span><span class="sxs-lookup"><span data-stu-id="80988-125">Double-click **Mailbox -  _[User Name]_** in the store table list view.</span></span> 
    
6. <span data-ttu-id="80988-126">Na exibição de árvore de pastas, expanda o nó raiz.</span><span class="sxs-lookup"><span data-stu-id="80988-126">In the folder tree view, expand the root node.</span></span> <span data-ttu-id="80988-127">O nome exibido para o nó raiz varia dependendo do tipo de perfil selecionado.</span><span class="sxs-lookup"><span data-stu-id="80988-127">The name displayed for the root node varies depending on the type of profile selected.</span></span> <span data-ttu-id="80988-128">Normalmente, esse nó é exibido como **Raiz - Caixa de Correio.**</span><span class="sxs-lookup"><span data-stu-id="80988-128">Typically this node is displayed as **Root - Mailbox**.</span></span>
    
7. <span data-ttu-id="80988-129">Na exibição de árvore de pastas, expanda o nó que contém o armazenamento de informações.</span><span class="sxs-lookup"><span data-stu-id="80988-129">In the folder tree view, expand the node that contains the information store.</span></span> <span data-ttu-id="80988-130">O nome exibido para esse nó varia dependendo do tipo de perfil selecionado.</span><span class="sxs-lookup"><span data-stu-id="80988-130">The name displayed for this node varies depending on the type of profile selected.</span></span> <span data-ttu-id="80988-131">Normalmente, esse nó é exibido como **IPM_SUBTREE** ou Início do Armazenamento **de Informações.**</span><span class="sxs-lookup"><span data-stu-id="80988-131">Typically this node is displayed as **IPM_SUBTREE** or **Top of Information Store**.</span></span>
    
8. <span data-ttu-id="80988-132">Clique duas vezes na pasta para o tipo de item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="80988-132">Double-click the folder for the item type to create.</span></span> <span data-ttu-id="80988-133">Por exemplo, para criar um compromisso, clique na **pasta Compromissos.**</span><span class="sxs-lookup"><span data-stu-id="80988-133">For example, to create an appointment, click the **Appointments** folder.</span></span> 
    
9. <span data-ttu-id="80988-134">No menu **Addins,** clique no comando apropriado para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="80988-134">On the **Addins** menu, click the appropriate command for the item to create.</span></span> 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a><span data-ttu-id="80988-135">Baixar e exibir o código do aplicativo MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80988-135">Download and view code from the MFCMAPI application</span></span>

<span data-ttu-id="80988-136">Alguns tópicos se referem ao código-fonte do próprio aplicativo MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="80988-136">Some topics refer to source code from the MFCMAPI application itself.</span></span> <span data-ttu-id="80988-137">As etapas a seguir descrevem como baixar o código-fonte MFCMAPI e exibi-lo no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="80988-137">The following steps describe how to download the MFCMAPI source code and view it in Visual Studio.</span></span> 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a><span data-ttu-id="80988-138">Para baixar e exibir o código-fonte do aplicativo MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80988-138">To download and view the MFCMAPI application source code</span></span>

1. <span data-ttu-id="80988-139">Baixe o código-fonte da versão atual do [aplicativo MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) para uma pasta em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="80988-139">Download the source code for the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) application to a folder on your system.</span></span> 
    
2. <span data-ttu-id="80988-140">Extraia os arquivos em MFCMAPI - _changeset_.zip para uma pasta vazia no disco rígido.</span><span class="sxs-lookup"><span data-stu-id="80988-140">Extract the files in MFCMAPI- _changeset_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="80988-141">Abra o projeto MFCMapi (\ _foldername_\ MFCMapi.vcproj) no Visual Studio para examinar o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="80988-141">Open the MFCMapi project (\ _foldername_\ MFCMapi.vcproj) in Visual Studio to examine the source code.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="80988-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="80988-142">See also</span></span>

- [<span data-ttu-id="80988-143">Criar um Item de Email Simples</span><span class="sxs-lookup"><span data-stu-id="80988-143">Create a Simple Mail Item</span></span>](how-to-create-a-simple-mail-item.md)
- [<span data-ttu-id="80988-144">Criar um item de tarefa recorrente simples</span><span class="sxs-lookup"><span data-stu-id="80988-144">Create a Simple Recurrent Task Item</span></span>](how-to-create-a-simple-recurrent-task-item.md)
- [<span data-ttu-id="80988-145">Criar um item de compromisso recorrente complexo</span><span class="sxs-lookup"><span data-stu-id="80988-145">Create a Complex Recurrent Appointment Item</span></span>](how-to-create-a-complex-recurrent-appointment-item.md)
- [<span data-ttu-id="80988-146">Ler e analisar um padrão de recorrência</span><span class="sxs-lookup"><span data-stu-id="80988-146">Read and Parse a Recurrence Pattern</span></span>](how-to-read-and-parse-a-recurrence-pattern.md)

