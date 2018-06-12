---
title: Sobre como definir a ordem de resolu��o de listas de endere�os no Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766088"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Sobre como definir a ordem de resolu��o de listas de endere�os no Outlook

  
  
**Aplica-se a**: Outlook 
  
Para cada perfil, Microsoft Office Outlook oferece suporte a várias listas de endereços e os usuários podem especificar manualmente a ordem das listas de endereços pelos quais destinatários em email participantes em solicitações de reunião e mensagens forem resolvidos. Por exemplo, voc� pode definir a ordem de resolu��o para que os nomes ser�o resolvidos primeiro contra seu cat�logo de endere�os do Outlook e, em seguida, a lista de endere�os Global. Em um computador, um usu�rio pode abrir o cat�logo de endere�os, clique em **Ferramentas** e em seguida **Op��es** para especificar nesta ordem de resolu��o. No entanto, em um ambiente corporativo, � mais eficiente para administradores de TI definir programaticamente a ordem das listas de endere�os pelo qual nomes forem resolvidos. Esse tipo de c�digo pode ser usado como parte de um script de automa��o de inicializa��o que um administrador implanta dentro da corpora��o. 
  
MAPI oferece suporte ao m�todo **[SetSearchPath](iaddrbook-getsearchpath.md)** na interface do **[IAddrBook](iaddrbookimapiprop.md)**, que permite que voc� defina um novo caminho de pesquisa no perfil que ser� usado para resolu��o de nome. Para usar o m�todo **IAddrBook::SetSearchPath**, voc� deve especificar a ordem de resolu��o desejada usando uma matriz que cont�m os cont�ineres do endere�o relevante manuais online na ordem que eles devem ser resolvidos. Cada entrada nessa matriz tamb�m deve conter a identifica��o de entrada do cat�logo de endere�os correspondente. 
  
A seguir est�o exemplos de c�digo de como especificar um caminho de pesquisa personalizada para listas de endere�os.
  
- [Definir a ordem de resolução de listas de endereços de forma programática](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: como alterar a ordem de classifica��o do cat�logo de endere�os com SetSearchPath](http://support.microsoft.com/kb/292590)
    

