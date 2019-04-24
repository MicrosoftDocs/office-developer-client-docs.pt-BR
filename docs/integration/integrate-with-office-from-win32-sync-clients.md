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
# <a name="integrate-with-office-from-win32-sync-clients"></a>Integração com o Office de clientes de sincronização do Win32

Integre seus clientes de sincronização Win32 de terceiros com aplicativos do Office como Word Mobile, Excel Mobile e PowerPoint Mobile. 
  
Você pode integrar seu aplicativo universal do Windows com os clientes do Word Mobile, Excel Mobile e PowerPoint Mobile registrando-o como provedor de raiz de sincronização. Este artigo descreve as práticas recomendadas a aplicar para garantir que seus clientes de sincronização Win32 funcionam bem com os aplicativos do Office.
  
Esta integração requer que o cliente de sincronização Win32 tenha um mecanismo de sincronização.
  
## <a name="register-as-a-sync-root-provider"></a>Registrar como um provedor de raiz de sincronização

A menos que o cliente de sincronização esteja registrado como um provedor de raiz de sincronização, o Office tratará arquivos na pasta de sincronização da forma que trata arquivos locais regulares. Isso significa que o Office fornecerá opções "Mover para o OneDrive" para usuários quando eles tentarem compartilhar o documento. Para evitar isso nos arquivos que você sincroniza, você deverá se registrar como provedor de raiz de sincronização. Para informações sobre como registrar, confira [Integrar um provedor de armazenamento em nuvem](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Integrar seu aplicativo no nó raiz do painel de navegação

Para que seu cliente de sincronização Win32 apareça como um nó raiz no painel de navegação no Explorador de Arquivos e no seletor de arquivos do Windows, você precisa integrar seu aplicativo ao nível raiz. Para saber mais sobre como fazer isso, confira [Integrar um provedor de armazenamento em nuvem](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Adicionar a sua pasta de sincronização como uma biblioteca de documentos (opcional)

No Office, os usuários podem criar documentos em suas bibliotecas de documentos com uma única ação. Para adicionar seu local de sincronização à biblioteca de documentos, use a função [SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>Confira também
<a name="bk_addresources"> </a>

- [Integração com o Office](integrate-with-office.md)
    
- [Integração com o Office em aplicativos universais do Windows](integrate-with-office-from-windows-universal-apps.md)
    

