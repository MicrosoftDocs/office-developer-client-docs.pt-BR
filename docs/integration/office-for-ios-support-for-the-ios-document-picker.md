---
title: Suporte do Office para iOS para o seletor de documentos do iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: O Office para iOS se integra ao Seletor de Documentos do iOS por meio da extensão do Provedor de Documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410662"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="df702-103">Suporte do Office para iOS para o seletor de documentos do iOS</span><span class="sxs-lookup"><span data-stu-id="df702-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="df702-104">O Office para iOS se integra ao Seletor de Documentos do iOS por meio da extensão do Provedor de Documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="df702-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="df702-105">As versões do Apple iOS a partir do iOS 8.0 incluem [suporte à extensão de aplicativo.](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)</span><span class="sxs-lookup"><span data-stu-id="df702-105">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1).</span></span> <span data-ttu-id="df702-106">Você pode usar essas extensões para expandir a funcionalidade do seu aplicativo para outros aplicativos ou contextos no dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="df702-106">You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device.</span></span> <span data-ttu-id="df702-107">Para integrar o Office para iOS com o Seletor de Documentos do iOS, use a extensão [do Provedor de Documentos.](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)</span><span class="sxs-lookup"><span data-stu-id="df702-107">To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="df702-108">A extensão do Provedor de Documentos oferece suporte a quatro operações:</span><span class="sxs-lookup"><span data-stu-id="df702-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="df702-109">Importar</span><span class="sxs-lookup"><span data-stu-id="df702-109">Import</span></span>
    
- <span data-ttu-id="df702-110">Exportar</span><span class="sxs-lookup"><span data-stu-id="df702-110">Export</span></span>
    
- <span data-ttu-id="df702-111">Abrir</span><span class="sxs-lookup"><span data-stu-id="df702-111">Open</span></span>
    
- <span data-ttu-id="df702-112">Mover</span><span class="sxs-lookup"><span data-stu-id="df702-112">Move</span></span>
    
<span data-ttu-id="df702-113">O Office para iOS se integra à operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="df702-113">Office for iOS integrates with the open operation.</span></span> <span data-ttu-id="df702-114">Quando você cria uma extensão de Provedor de Documentos, os usuários podem usar o Selador de Documentos para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.</span><span class="sxs-lookup"><span data-stu-id="df702-114">When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="df702-115">Saiba mais sobre extensões de aplicativos e o Selador de Documento</span><span class="sxs-lookup"><span data-stu-id="df702-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="df702-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="df702-116"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="df702-117">Extensões de aplicativo</span><span class="sxs-lookup"><span data-stu-id="df702-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="df702-118">Guia de programação do selador de documentos</span><span class="sxs-lookup"><span data-stu-id="df702-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="df702-119">Guia de programação do provedor de documentos</span><span class="sxs-lookup"><span data-stu-id="df702-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

