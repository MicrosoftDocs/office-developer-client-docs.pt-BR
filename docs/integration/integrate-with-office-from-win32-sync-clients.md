---
title: Integração com o Office de clientes de sincronização do Win32
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Integre seus clientes de sincronização Win32 de terceiros com aplicativos do Office como Word Mobile, Excel Mobile e PowerPoint Mobile.
ms.openlocfilehash: 83bc6e4cddc17e539b371999fff620c72c595534
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303133"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="c4c8b-103">Integração com o Office de clientes de sincronização do Win32</span><span class="sxs-lookup"><span data-stu-id="c4c8b-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="c4c8b-104">Integre seus clientes de sincronização Win32 de terceiros com aplicativos do Office como Word Mobile, Excel Mobile e PowerPoint Mobile.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="c4c8b-105">Você pode integrar seu aplicativo universal do Windows com os clientes do Word Mobile, Excel Mobile e PowerPoint Mobile registrando-o como provedor de raiz de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-105">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider.</span></span> <span data-ttu-id="c4c8b-106">Este artigo descreve as práticas recomendadas a aplicar para garantir que seus clientes de sincronização Win32 funcionam bem com os aplicativos do Office.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-106">This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="c4c8b-107">Esta integração requer que o cliente de sincronização Win32 tenha um mecanismo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="c4c8b-108">Registrar como um provedor de raiz de sincronização</span><span class="sxs-lookup"><span data-stu-id="c4c8b-108">Register as a sync root provider</span></span>

<span data-ttu-id="c4c8b-109">A menos que o cliente de sincronização esteja registrado como um provedor de raiz de sincronização, o Office tratará arquivos na pasta de sincronização da forma que trata arquivos locais regulares.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-109">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files.</span></span> <span data-ttu-id="c4c8b-110">Isso significa que o Office fornecerá opções "Mover para o OneDrive" para usuários quando eles tentarem compartilhar o documento.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-110">This means that Office will provide "move to OneDrive" options for users when they attempt to share the document.</span></span> <span data-ttu-id="c4c8b-111">Para evitar isso nos arquivos que você sincroniza, você deverá se registrar como provedor de raiz de sincronização.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-111">To avoid this for files you sync, you must register as a sync root provider.</span></span> <span data-ttu-id="c4c8b-112">Para informações sobre como registrar, confira [Integrar um provedor de armazenamento em nuvem](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4c8b-112">For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="c4c8b-113">Integrar seu aplicativo no nó raiz do painel de navegação</span><span class="sxs-lookup"><span data-stu-id="c4c8b-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="c4c8b-114">Para que seu cliente de sincronização Win32 apareça como um nó raiz no painel de navegação no Explorador de Arquivos e no seletor de arquivos do Windows, você precisa integrar seu aplicativo ao nível raiz.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-114">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level.</span></span> <span data-ttu-id="c4c8b-115">Para saber mais sobre como fazer isso, confira [Integrar um provedor de armazenamento em nuvem](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4c8b-115">For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="c4c8b-116">Adicionar a sua pasta de sincronização como uma biblioteca de documentos (opcional)</span><span class="sxs-lookup"><span data-stu-id="c4c8b-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="c4c8b-117">No Office, os usuários podem criar documentos em suas bibliotecas de documentos com uma única ação.</span><span class="sxs-lookup"><span data-stu-id="c4c8b-117">In Office, users can create documents in their document libraries with a single action.</span></span> <span data-ttu-id="c4c8b-118">Para adicionar seu local de sincronização à biblioteca de documentos, use a função [SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4c8b-118">To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4c8b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4c8b-119">See also</span></span>
<span data-ttu-id="c4c8b-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="c4c8b-120"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="c4c8b-121">Integração com o Office</span><span class="sxs-lookup"><span data-stu-id="c4c8b-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="c4c8b-122">Integração com o Office em aplicativos universais do Windows</span><span class="sxs-lookup"><span data-stu-id="c4c8b-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

