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
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Suporte do Office para iOS para o seletor de documentos do iOS

O Office para iOS se integra ao Seletor de Documentos do iOS por meio da extensão do Provedor de Documentos, que permite ao Office abrir arquivos armazenados por outro provedor de documentos.
  
As versões do Apple iOS a partir do iOS 8.0 incluem [suporte à extensão de aplicativo.](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1) Você pode usar essas extensões para expandir a funcionalidade do seu aplicativo para outros aplicativos ou contextos no dispositivo do usuário. Para integrar o Office para iOS com o Seletor de Documentos do iOS, use a extensão [do Provedor de Documentos.](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
  
A extensão do Provedor de Documentos oferece suporte a quatro operações:
  
- Importar
    
- Exportar
    
- Abrir
    
- Mover
    
O Office para iOS se integra à operação de abertura. Quando você cria uma extensão de Provedor de Documentos, os usuários podem usar o Selador de Documentos para abrir e editar documentos diretamente no Office sem criar uma cópia duplicada do arquivo.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>Saiba mais sobre extensões de aplicativos e o Selador de Documento
<a name="bk_addresources"> </a>

- [Extensões de aplicativo](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Guia de programação do selador de documentos](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Guia de programação do provedor de documentos](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

