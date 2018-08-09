---
title: Provedores de serviços MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3f1cab24ef6bbd632ee3dc204e93f59e6f9ac846
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767958"
---
# <a name="mapi-service-providers"></a>Provedores de serviços MAPI

  
  
**Aplica-se a**: Outlook 
  
Existem três tipos comuns de provedores de serviços:
  
- Provedores de catálogo de endereços.
    
- Provedores de armazenamento de mensagem.
    
- Provedores de transporte.
    
Provedores de armazenamento de mensagens e catálogo de endereço têm muitas semelhanças. Eles registram um identificador exclusivo com MAPI empregados para construir identificadores de entrada para seus objetos. Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular. Para seus objetos de contêiner, eles suportam uma tabela de hierarquia e uma tabela de conteúdo. Eles suportam notificação de evento nestas tabelas e, opcionalmente, em objetos individuais para que os clientes podem ser informados sobre alterações que ocorrem durante a sessão. Quando operações ficam longas, eles podem exibir um indicador de progresso para informar ao usuário sobre o status da operação. Os clientes podem se comunicar com provedores de armazenamento de mensagens e catálogo de endereço qualquer MAPI indiretamente até usando o [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession: IUnknown](imapisessioniunknown.md) interfaces ou diretamente usando com uma das interfaces do provedor de serviço no tabela a seguir. 
  
|**Interfaces do provedor de catálogo de endereços**|**Interfaces do provedor de repositório de mensagem**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Provedores de transporte diferem dos provedores de armazenamento mensagens e catálogo de endereço da maneira que se comunicam com MAPI e com clientes. Provedores de transporte normalmente Aguarde MAPI-los solicitar informações ao invés de iniciar a comunicação. Ao contrário de outros provedores, provedores de transporte não suportam uma variedade de objetos e tabelas que costumam ser acessadas pelos clientes. No entanto, eles têm suporte para um objeto de status, conforme faça todos os provedores de serviço e publicar suas propriedades da tabela de status. Enquanto os provedores de armazenamento de mensagens e catálogo de endereço chamarem o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar os identificadores exclusivos para construir seus identificadores de entrada, chamarem o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para ThisDocument provedores de transporte Registre os identificadores exclusivos, bem como tipos de endereço de assumindo a responsabilidade para a entrega de mensagens específicas. 
  
Seu provedor de serviços deve ter os três arquivos de cabeçalho: um arquivo de cabeçalho público e dois arquivos internos. Use o arquivo de cabeçalho público para a configuração e para documentar as propriedades e seus valores. Incluir em um dos arquivos de cabeçalho interno todos os necessário pública MAPI cabeçalhos; Este arquivo de cabeçalho deve ser incluído em todos os seus arquivos de origem de provedor de serviço. Use o outro arquivo interno para definir os identificadores de recurso.
  
Catálogo de endereços, armazenamento de mensagens e provedores de transporte executam as seguintes tarefas:
  
- Fornece uma função de ponto de entrada. 
    
- Fornece um provedor e o objeto de logon para lidar com o logon e inicialização. 
    
- Se o provedor pertence a um serviço de mensagem, fornece uma função de ponto de entrada de serviço de mensagens. 
    
- Suporte a configuração por meio da implementação de uma folha de propriedades.
    
- Um objeto de status de implementar e oferecer suporte a tabela de status. 
    
- Alça desligado.
    
## <a name="see-also"></a>Confira também



[Conceitos MAPI](mapi-concepts.md)

