---
title: Provedores de serviço MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346673"
---
# <a name="mapi-service-providers"></a>Provedores de serviço MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há três tipos comuns de provedores de serviços:
  
- Provedores de catálogos de endereços.
    
- Provedores do repositório de mensagens.
    
- Provedores de transporte.
    
Os provedores de catálogo de endereços e de repositório de mensagens têm muitas semelhanças. Eles registram um identificador exclusivo com MAPI que eles usam para construir identificadores de entrada para seus objetos. Eles fornecem uma hierarquia de objetos e propriedades que os clientes podem acessar e manipular. Para seus objetos contêiner, eles dão suporte a uma tabela de hierarquia e a uma tabela de conteúdo. Eles dão suporte à notificação de eventos nessas tabelas e, opcionalmente, em objetos individuais para que os clientes possam ser informados sobre alterações que ocorrem durante a sessão. Quando as operações se tornam longas, elas podem exibir um indicador de progresso para informar o usuário sobre o status da operação. Os clientes podem se comunicar com o catálogo de endereços e os provedores de repositórios de mensagens indiretamente por meio de MAPI usando as interfaces [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) e [IMAPISession: IUnknown](imapisessioniunknown.md) ou diretamente usando uma das interfaces de provedor de serviços no tabela a seguir. 
  
|**Interfaces do provedor de catálogo de endereços**|**Interfaces do provedor de repositório de mensagens**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage : IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
Os provedores de transporte diferem dos provedores de catálogo de endereços e de repositório de mensagens no modo como se comunicam com MAPI e com clientes. Geralmente, os provedores de transporte esperam por MAPI solicitar informações em vez de iniciar a comunicação. Diferentemente dos outros provedores, os provedores de transporte não dão suporte a uma variedade de objetos e tabelas que são comumente acessados por clientes. No enTanto, eles dão suporte a um objeto status, como todos os provedores de serviço e publica suas propriedades na tabela de status. Enquanto o catálogo de endereços e os provedores de repositório de mensagens chamam o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar identificadores exclusivos para construir seus identificadores de entrada, os provedores de transporte chamam o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) para Registre os identificadores exclusivos, bem como os tipos de endereço para assumir a responsabilidade da entrega de mensagens específicas. 
  
Seu provedor de serviços deve ter três arquivos de cabeçalho: um arquivo de cabeçalho público e dois arquivos internos. Use o arquivo de cabeçalho público para configuração e para documentar Propriedades e seus valores. Inclua um dos arquivos de cabeçalho internos todos os cabeçalhos MAPI públicos necessários; Esse arquivo de cabeçalho deve ser incluído em todos os arquivos de origem do provedor de serviços. Use o outro arquivo interno para definir identificadores de recurso.
  
Catálogo de endereços, repositório de mensagens e provedores de transporte execute as seguintes tarefas:
  
- Forneça uma função de ponto de entrada. 
    
- Forneça um provedor e um objeto de logon para manipular o logon e a inicialização. 
    
- Se o provedor pertencer a um serviço de mensagens, forneça uma função de ponto de entrada do serviço de mensagens. 
    
- Suporte à configuração implementando uma folha de propriedades.
    
- Implemente um objeto status e dê suporte à tabela status. 
    
- Controle de desligamento.
    
## <a name="see-also"></a>Confira também



[Conceitos de MAPI](mapi-concepts.md)

