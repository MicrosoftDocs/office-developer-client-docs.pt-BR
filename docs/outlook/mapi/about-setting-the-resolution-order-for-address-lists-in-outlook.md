---
title: Sobre como definir a ordem de resolução de listas de endereços no Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391406"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Sobre como definir a ordem de resolução de listas de endereços no Outlook

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para cada perfil, o Microsoft Office Outlook suporta várias listas de endereços e os usuários podem especificar manualmente a ordem das lista de endereços pelas quais são resolvidos os recebedores de mensagens de email e os participantes de solicitações de reunião. Por exemplo, você pode definir a ordem de resolução para que os nomes sejam resolvidos primeiro de acordo com seu Catálogo de Endereços do Outlook, e depois de acordo com a Lista de Endereços Global. Em um computador, um usuário pode abrir o catálogo de endereços, clicar em **Ferramentas** e, em seguida, em **Opções** para especificar esta ordem de resolução. No entanto, em um ambiente corporativo, é mais eficiente para os administradores de TI definir programaticamente a ordem das listas de endereços segundo a qual os nomes são resolvidos. Este código pode ser usado como parte de um script de automação de inicialização que um administrador implanta dentro da corporação. 
  
A MAPI suporta o método **[SetSearchPath](iaddrbook-getsearchpath.md)** na interface **[IAddrBook](iaddrbookimapiprop.md)**, o que permite que você defina um novo caminho de pesquisa no perfil usado para a resolução dos nomes. Para usar o método **IAddrBook::SetSearchPath**, você precisa especificar a ordem de resolução desejada usando uma matriz com contêineres dos catálogos de endereços relevantes na ordem em que eles devem ser resolvidos. Cada entrada nessa matriz também deve conter a ID de entrada do catálogo de endereços correspondente. 
  
A seguir estão exemplos de código de como especificar um caminho de pesquisa personalizado para catálogos de endereços.
  
- [Definir programaticamente a ordem de resolução para catálogos de endereços](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: Como alterar a ordem de classificação do catálogo de endereços com SetSearchPath](https://support.microsoft.com/kb/292590)
    

