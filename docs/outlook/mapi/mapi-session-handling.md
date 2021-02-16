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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422058"
---
# <a name="mapi-session-handling"></a>Manipulação de sessão MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Antes de poder se comunicar com provedores de serviços e um sistema de mensagens subjacente, você deve estabelecer uma sessão. Uma sessão MAPI é um link de um cliente para outros componentes MAPI. Como resultado do início bem-sucedido de uma sessão, o MAPI retorna aos clientes um ponteiro para um objeto de sessão — um objeto que implementa a interface **IMAPISession.** Para obter mais informações, [consulte IMAPISession : IUnknown](imapisessioniunknown.md). Você pode usar os métodos da interface **IMAPISession** para acessar os objetos do livro de endereços e provedores de armazenamento de mensagens, acessar várias tabelas, exibir formulários, definir propriedades do provedor de transporte e executar a administração de perfil e serviço de mensagens. 
  
## <a name="in-this-section"></a>Nesta seção

[Iniciando uma sessão MAPI](starting-a-mapi-session.md)
  
> Descreve como iniciar uma sessão MAPI e inclui links para tópicos com informações mais detalhadas.
    
[Encerrando uma sessão MAPI](ending-a-mapi-session.md)
  
> Descreve como encerrar uma sessão MAPI.
    
[Acessando objetos usando a sessão](accessing-objects-by-using-the-session.md)
  
> Descreve como usar um ponteiro de sessão para acessar objetos de sessão.
    
[Recuperando a identidade principal e do provedor](retrieving-primary-and-provider-identity.md)
  
> Descreve as propriedades usadas para recuperar a identidade principal e do provedor.
    
[Tabela de Status e Objetos de Status](status-table-and-status-objects.md)
  
> Descreve como acessar informações da tabela de status.
    

