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
# <a name="integrate-with-office-from-win32-sync-clients"></a>Integração com o Office em clientes de sincronização do Win32

Integre seus clientes de sincronização do Win32 de terceiros aplicativos móveis do Excel, PowerPoint Mobile e Word Mobile Office. 
  
É possível integrar seu aplicativo universal do Windows com clientes móveis do Excel, PowerPoint Mobile e Word Mobile registrando-se como um provedor de raiz de sincronização. Este artigo descreve as práticas recomendadas para aplicar para garantir que seus clientes de sincronização do Win32 funcionam bem com aplicativos do Office.
  
Essa integração requer que o seu cliente de sincronização do Win32 tem um mecanismo de sincronização.
  
## <a name="register-as-a-sync-root-provider"></a>Registrar como um provedor de sincronização de raiz

A menos que seu cliente de sincronização está registrado como um provedor de sincronização de raiz, Office tratará arquivos em sua pasta de sincronização a maneira que ele trata regulares arquivos locais. Isso significa que o Office fornecerá opções "Mover para o OneDrive" para os usuários quando eles tentam compartilhar o documento. Para evitar isso para sincronização de arquivos, você deve registrar como um provedor de raiz de sincronização. Para obter informações sobre como registrar, consulte [integra-se um provedor de armazenamento de nuvem](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Integrar seu aplicativo no nó raiz do painel de navegação

Para seu cliente de sincronização do Win32 apareça como um nó raiz no painel de navegação no selecionador de arquivo do Gerenciador de arquivos e o Windows, é necessário integrar o seu aplicativo no nível raiz. Para obter informações sobre como fazer isso, consulte [integra-se um provedor de armazenamento de nuvem](https://msdn.microsoft.com/en-us/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Adicione sua pasta de sincronização como uma biblioteca de documentos (opcional)

No Office, os usuários podem criar documentos em suas bibliotecas de documentos com uma única ação. Para adicionar o seu local de sincronização para a biblioteca de documentos, use a [função SHAddFolderPathToLibrary](https://msdn.microsoft.com/en-us/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [Integração com o Office em aplicativos universais do Windows](integrate-with-office-from-windows-universal-apps.md)
    

