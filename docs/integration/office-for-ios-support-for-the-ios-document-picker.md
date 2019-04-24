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
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Suporte do Office para iOS para o seletor de documentos do iOS

O Office para iOS integra-se com o seletor de documentos iOS por meio da extensão do provedor de documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
  
Versões do Apple iOS começando com iOS 8,0 incluem [suporte à extensão de aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Você pode usar essas extensões para expandir a funcionalidade do aplicativo em outros aplicativos ou contextos no dispositivo do usuário. Para integrar o Office para iOS com o seletor de documentos iOS, use a [extensão de provedor de documentos](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).
  
A extensão do provedor de documentos oferece suporte a quatro operações:
  
- Importar
    
- Exportar
    
- Abrir
    
- Mover
    
O Office para iOS integra-se com a operação abrir. Quando você cria uma extensão de provedor de documentos, os usuários podem usar o seletor de documentos para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>Saiba mais sobre extensões de aplicativos e o seletor de documentos
<a name="bk_addresources"> </a>

- [Extensões de aplicativos](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Guia de programação do seletor de documentos](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Guia de programação de provedor de documentos](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

