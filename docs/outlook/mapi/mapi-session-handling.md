---
title: Manipulação de sessão MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328221"
---
# <a name="mapi-session-handling"></a>Manipulação de sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para que você possa se comunicar com os provedores de serviço e um sistema de mensagens subjacente, você deve estabelecer uma sessão. Uma sessão MAPI é um link de um cliente para outros componentes MAPI. Como resultado da inicialização com êxito de uma sessão, o MAPI retorna aos clientes um ponteiro para um objeto Session — um objeto que implementa a interface **IMAPISession** . Para obter mais informações, consulte [IMAPISession: IUnknown](imapisessioniunknown.md). Você pode usar os métodos da interface **IMAPISession** para acessar os objetos do catálogo de endereços e provedores de repositório de mensagens, acessar várias tabelas, formulários de exibição, definir propriedades do provedor de transporte e realizar a administração de perfis e serviços de mensagens. 
  
## <a name="in-this-section"></a>Nesta seção

[Iniciar uma sessão MAPI](starting-a-mapi-session.md)
  
> Descreve como iniciar uma sessão MAPI e inclui links para tópicos com informações mais detalhadas.
    
[Finalizar uma sessão MAPI](ending-a-mapi-session.md)
  
> Descreve como finalizar uma sessão MAPI.
    
[Acessar objetos usando a sessão](accessing-objects-by-using-the-session.md)
  
> Descreve como usar um ponteiro de sessão para acessar objetos de sessão.
    
[Recuperar a identidade principal e do provedor](retrieving-primary-and-provider-identity.md)
  
> Descreve as propriedades usadas para recuperar a identidade principal e do provedor.
    
[Tabela de status e objetos de status](status-table-and-status-objects.md)
  
> Descreve como acessar informações da tabela status.
    

