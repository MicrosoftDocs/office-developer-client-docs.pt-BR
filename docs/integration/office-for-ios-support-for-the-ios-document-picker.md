---
title: Office para suporte de iOS para o iOS selecionador de documento
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office para iOS integra o iOS selecionador de documentos por meio de extensão do provedor de documento, que permite que o Office abrir arquivos armazenados por outro provedor do documento.
ms.openlocfilehash: 101e3cc248f994fe449a74c6c37f788fad8beed5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765759"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a><span data-ttu-id="cdb29-103">Office para suporte de iOS para o iOS selecionador de documento</span><span class="sxs-lookup"><span data-stu-id="cdb29-103">Office for iOS support for the iOS Document Picker</span></span>

<span data-ttu-id="cdb29-104">Office para iOS integra o iOS selecionador de documentos por meio de extensão do provedor de documento, que permite que o Office abrir arquivos armazenados por outro provedor do documento.</span><span class="sxs-lookup"><span data-stu-id="cdb29-104">Office for iOS integrates with the iOS Document Picker by means of the Document Provider extension, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="cdb29-105">Versões do Apple iOS começando com iOS 8.0 incluem o [suporte a extensão do aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1).</span><span class="sxs-lookup"><span data-stu-id="cdb29-105">Versions of the Apple iOS starting with iOS 8.0 include [app extension support](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1).</span></span> <span data-ttu-id="cdb29-106">Você pode usar essas extensões para expandir a funcionalidade do seu aplicativo em outros aplicativos ou contextos no dispositivo do usuário.</span><span class="sxs-lookup"><span data-stu-id="cdb29-106">You can use these extensions to expand the functionality of your application into other apps or contexts on the user's device.</span></span> <span data-ttu-id="cdb29-107">Para integrar o Office para iOS com o iOS selecionador de documento, você deve usar a [extensão do provedor do documento](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span><span class="sxs-lookup"><span data-stu-id="cdb29-107">To integrate Office for iOS with the iOS Document Picker, you use the [Document Provider extension](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).</span></span>
  
<span data-ttu-id="cdb29-108">A extensão do provedor de documento suporta quatro operações:</span><span class="sxs-lookup"><span data-stu-id="cdb29-108">The Document Provider extension supports four operations:</span></span>
  
- <span data-ttu-id="cdb29-109">Importação</span><span class="sxs-lookup"><span data-stu-id="cdb29-109">Import</span></span>
    
- <span data-ttu-id="cdb29-110">Exportar</span><span class="sxs-lookup"><span data-stu-id="cdb29-110">Export</span></span>
    
- <span data-ttu-id="cdb29-111">Abrir</span><span class="sxs-lookup"><span data-stu-id="cdb29-111">Open</span></span>
    
- <span data-ttu-id="cdb29-112">Mover</span><span class="sxs-lookup"><span data-stu-id="cdb29-112">Move</span></span>
    
<span data-ttu-id="cdb29-113">Office para iOS integra-se a operação aberta.</span><span class="sxs-lookup"><span data-stu-id="cdb29-113">Office for iOS integrates with the open operation.</span></span> <span data-ttu-id="cdb29-114">Quando você cria uma extensão do provedor de documento, os usuários podem usar o seletor de documento para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cdb29-114">When you create a Document Provider extension, your users can use the Document Picker to open and edit documents directly in Office without creating a duplicate copy of the file.</span></span>
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a><span data-ttu-id="cdb29-115">Saiba mais sobre as extensões de aplicativo e o seletor de documento</span><span class="sxs-lookup"><span data-stu-id="cdb29-115">Learn more about app extensions and the Document Picker</span></span>
<span data-ttu-id="cdb29-116"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="cdb29-116"></span></span>

- [<span data-ttu-id="cdb29-117">Extensões de aplicativo</span><span class="sxs-lookup"><span data-stu-id="cdb29-117">App extensions</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [<span data-ttu-id="cdb29-118">Guia de programação do seletor de documento</span><span class="sxs-lookup"><span data-stu-id="cdb29-118">Document Picker Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [<span data-ttu-id="cdb29-119">Guia de programação do provedor de documento</span><span class="sxs-lookup"><span data-stu-id="cdb29-119">Document Provider Programming Guide</span></span>](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

