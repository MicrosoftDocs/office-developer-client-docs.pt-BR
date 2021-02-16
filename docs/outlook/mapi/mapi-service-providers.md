---
title: Provedores de Serviços MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409535"
---
# <a name="mapi-service-providers"></a>Provedores de Serviços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Existem três tipos comuns de provedores de serviços:
  
- Provedores de lista de endereços.
    
- Provedores de armazenamento de mensagens.
    
- Provedores de transporte.
    
Os provedores de armazenamento de mensagens e de address book têm muitas semelhanças. Eles registram um identificador exclusivo com MAPI que usam para construir identificadores de entrada para seus objetos. Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular. Para seus objetos contêineres, eles suportam uma tabela de hierarquia e uma tabela de conteúdo. Eles suportam a notificação de evento nessas tabelas e, opcionalmente, em objetos individuais, para que os clientes possam ser informados das alterações que ocorrem durante a sessão. Quando as operações se tornam demoradas, elas podem exibir um indicador de progresso para informar o usuário sobre o status da operação. Os clientes podem se comunicar com o livro de endereços e provedores de armazenamento de mensagens indiretamente através de MAPI usando [o IAddrBook : IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession : interfaces IUnknown](imapisessioniunknown.md) ou diretamente usando uma das interfaces do provedor de serviços na tabela a seguir. 
  
|**Interfaces do provedor de agendas**|**Interfaces do provedor do armazenamento de mensagens**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Os provedores de transporte diferem do livro de endereços e dos provedores de armazenamento de mensagens na maneira como se comunicam com MAPI e com clientes. Os provedores de transporte normalmente aguardam o MAPI solicitar informações em vez de iniciar a comunicação. Ao contrário dos outros provedores, os provedores de transporte não suportam uma variedade de objetos e tabelas que são comumente acessados por clientes. No entanto, eles suportam um objeto de status, assim como todos os provedores de serviços, e publicam suas propriedades na tabela de status. Enquanto os provedores de armazenamento de mensagens e de agendamento de endereços chamam o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores exclusivos para construir seus identificadores de entrada, os provedores de transporte chamam o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para registrar identificadores exclusivos, bem como os tipos de endereço para assumir a responsabilidade pela entrega de mensagens específicas. 
  
Seu provedor de serviços deve ter três arquivos de header: um arquivo de header público e dois arquivos internos. Use o arquivo de header público para configuração e para documentar propriedades e seus valores. Inclua em um dos arquivos de header internos todos os headers DE MAPI públicos necessários; esse arquivo de header deve ser incluído em todos os arquivos de origem do provedor de serviços. Use o outro arquivo interno para definir identificadores de recurso.
  
Os provedores de agenda, armazenamento de mensagens e transporte executam as seguintes tarefas:
  
- Fornecer uma função de ponto de entrada. 
    
- Fornecer um provedor e um objeto de logon para lidar com o logon e a inicialização. 
    
- Se o provedor pertencer a um serviço de mensagens, fornecerá uma função de ponto de entrada do serviço de mensagens. 
    
- Suporte à configuração implementando uma folha de propriedades.
    
- Implemente um objeto de status e suporte a tabela de status. 
    
- Tratar o desligar.
    
## <a name="see-also"></a>Confira também



[Conceitos de MAPI](mapi-concepts.md)

