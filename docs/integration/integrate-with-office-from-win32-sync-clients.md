---
title: Integração com o Office em clientes de sincronização do Win32
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Integre seus clientes de sincronização do Win32 de terceiros aplicativos móveis do Excel, PowerPoint Mobile e Word Mobile Office.
ms.openlocfilehash: 9f520ad36583a9aa7cd73638fe92158f70d13daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765727"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="53dc2-103">Integração com o Office em clientes de sincronização do Win32</span><span class="sxs-lookup"><span data-stu-id="53dc2-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="53dc2-104">Integre seus clientes de sincronização do Win32 de terceiros aplicativos móveis do Excel, PowerPoint Mobile e Word Mobile Office.</span><span class="sxs-lookup"><span data-stu-id="53dc2-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="53dc2-105">É possível integrar seu aplicativo universal do Windows com clientes móveis do Excel, PowerPoint Mobile e Word Mobile registrando-se como um provedor de raiz de sincronização.</span><span class="sxs-lookup"><span data-stu-id="53dc2-105">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider.</span></span> <span data-ttu-id="53dc2-106">Este artigo descreve as práticas recomendadas para aplicar para garantir que seus clientes de sincronização do Win32 funcionam bem com aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="53dc2-106">This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="53dc2-107">Essa integração requer que o seu cliente de sincronização do Win32 tem um mecanismo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="53dc2-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="53dc2-108">Registrar como um provedor de sincronização de raiz</span><span class="sxs-lookup"><span data-stu-id="53dc2-108">Register as a sync root provider</span></span>

<span data-ttu-id="53dc2-109">A menos que seu cliente de sincronização está registrado como um provedor de sincronização de raiz, Office tratará arquivos em sua pasta de sincronização a maneira que ele trata regulares arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="53dc2-109">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files.</span></span> <span data-ttu-id="53dc2-110">Isso significa que o Office fornecerá opções "Mover para o OneDrive" para os usuários quando eles tentam compartilhar o documento.</span><span class="sxs-lookup"><span data-stu-id="53dc2-110">This means that Office will provide "move to OneDrive" options for users when they attempt to share the document.</span></span> <span data-ttu-id="53dc2-111">Para evitar isso para sincronização de arquivos, você deve registrar como um provedor de raiz de sincronização.</span><span class="sxs-lookup"><span data-stu-id="53dc2-111">To avoid this for files you sync, you must register as a sync root provider.</span></span> <span data-ttu-id="53dc2-112">Para obter informações sobre como registrar, consulte [integra-se um provedor de armazenamento de nuvem](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="53dc2-112">For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="53dc2-113">Integrar seu aplicativo no nó raiz do painel de navegação</span><span class="sxs-lookup"><span data-stu-id="53dc2-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="53dc2-114">Para seu cliente de sincronização do Win32 apareça como um nó raiz no painel de navegação no selecionador de arquivo do Gerenciador de arquivos e o Windows, é necessário integrar o seu aplicativo no nível raiz.</span><span class="sxs-lookup"><span data-stu-id="53dc2-114">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level.</span></span> <span data-ttu-id="53dc2-115">Para obter informações sobre como fazer isso, consulte [integra-se um provedor de armazenamento de nuvem](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="53dc2-115">For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="53dc2-116">Adicione sua pasta de sincronização como uma biblioteca de documentos (opcional)</span><span class="sxs-lookup"><span data-stu-id="53dc2-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="53dc2-117">No Office, os usuários podem criar documentos em suas bibliotecas de documentos com uma única ação.</span><span class="sxs-lookup"><span data-stu-id="53dc2-117">In Office, users can create documents in their document libraries with a single action.</span></span> <span data-ttu-id="53dc2-118">Para adicionar o seu local de sincronização para a biblioteca de documentos, use a [função SHAddFolderPathToLibrary](https://msdn.microsoft.com/en-us/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="53dc2-118">To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/en-us/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53dc2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="53dc2-119">See also</span></span>
<span data-ttu-id="53dc2-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="53dc2-120"></span></span>

- [<span data-ttu-id="53dc2-121">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="53dc2-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="53dc2-122">Integração com o Office em aplicativos universais do Windows</span><span class="sxs-lookup"><span data-stu-id="53dc2-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

