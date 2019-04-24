---
title: Suporte do Office para iOS para o seletor de documentos do iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: O Office para iOS integra-se com o seletor de documentos iOS por meio da extensão do provedor de documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299801"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="31a63-103">Suporte do Office para iOS para o seletor de documentos do iOS</span><span class="sxs-lookup"><span data-stu-id="31a63-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="31a63-104">O Office para iOS integra-se com o seletor de documentos iOS por meio da extensão do provedor de documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="31a63-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="31a63-105">Versões do Apple iOS começando com iOS 8,0 incluem [suporte à extensão de aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1).</span><span class="sxs-lookup"><span data-stu-id="31a63-105">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1).</span></span> <span data-ttu-id="31a63-106">Você pode usar essas extensões para expandir a funcionalidade do aplicativo em outros aplicativos ou contextos no dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="31a63-106">You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device.</span></span> <span data-ttu-id="31a63-107">Para integrar o Office para iOS com o seletor de documentos iOS, use a [extensão de provedor de documentos](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span><span class="sxs-lookup"><span data-stu-id="31a63-107">To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="31a63-108">A extensão do provedor de documentos oferece suporte a quatro operações:</span><span class="sxs-lookup"><span data-stu-id="31a63-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="31a63-109">Importar</span><span class="sxs-lookup"><span data-stu-id="31a63-109">Import</span></span>
    
- <span data-ttu-id="31a63-110">Exportar</span><span class="sxs-lookup"><span data-stu-id="31a63-110">Export</span></span>
    
- <span data-ttu-id="31a63-111">Abrir</span><span class="sxs-lookup"><span data-stu-id="31a63-111">Open</span></span>
    
- <span data-ttu-id="31a63-112">Mover</span><span class="sxs-lookup"><span data-stu-id="31a63-112">Move</span></span>
    
<span data-ttu-id="31a63-113">O Office para iOS integra-se com a operação abrir.</span><span class="sxs-lookup"><span data-stu-id="31a63-113">Office for iOS integrates with the open operation.</span></span> <span data-ttu-id="31a63-114">Quando você cria uma extensão de provedor de documentos, os usuários podem usar o seletor de documentos para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.</span><span class="sxs-lookup"><span data-stu-id="31a63-114">When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="31a63-115">Saiba mais sobre extensões de aplicativos e o seletor de documentos</span><span class="sxs-lookup"><span data-stu-id="31a63-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="31a63-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="31a63-116"></span></span>

- [<span data-ttu-id="31a63-117">Extensões de aplicativos</span><span class="sxs-lookup"><span data-stu-id="31a63-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="31a63-118">Guia de programação do seletor de documentos</span><span class="sxs-lookup"><span data-stu-id="31a63-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="31a63-119">Guia de programação de provedor de documentos</span><span class="sxs-lookup"><span data-stu-id="31a63-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

