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
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Office para suporte de iOS para o iOS selecionador de documento

Office para iOS integra o iOS selecionador de documentos por meio de extensão do provedor de documento, que permite que o Office abrir arquivos armazenados por outro provedor do documento.
  
Versões do Apple iOS começando com iOS 8.0 incluem o [suporte a extensão do aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Você pode usar essas extensões para expandir a funcionalidade do seu aplicativo em outros aplicativos ou contextos no dispositivo do usuário. Para integrar o Office para iOS com o iOS selecionador de documento, você deve usar a [extensão do provedor do documento](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).
  
A extensão do provedor de documento suporta quatro operações:
  
- Importação
    
- Export
    
- Abrir
    
- Mover
    
Office para iOS integra-se a operação aberta. Quando você cria uma extensão do provedor de documento, os usuários podem usar o seletor de documento para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>Saiba mais sobre as extensões de aplicativo e o seletor de documento
<a name="bk_addresources"> </a>

- [Extensões de aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Guia de programação do seletor de documento](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Guia de programação do provedor de documento](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

