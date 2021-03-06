---
title: Recuperar propriedades MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417081"
---
# <a name="retrieving-mapi-properties"></a>Recuperar propriedades MAPI

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um cliente ou provedor de serviços recupera uma propriedade de um objeto, o objeto disponibiliza o valor, o tipo e o identificador da propriedade. 
  
Os clientes e provedores de serviços podem recuperar as propriedades de um objeto chamando um dos seguintes:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
O **método GetProps** é usado para recuperar uma ou mais propriedades que não precisam de uma interface especializada ou alternativa para acesso. Isso significa que as propriedades disponíveis com **GetProps** são pequenas, como números inteiros e valores booleano. 
  
 **Para recuperar várias propriedades**
  
1. Aloce [uma estrutura SPropTagArray](sproptagarray.md) grande o suficiente para manter o número de propriedades a serem recuperadas. 
    
2. Definir o membro **cValues** da estrutura **SPropTagArray** para o número de propriedades a serem recuperadas e definir cada membro **aulPropTag** para o identificador e tipo, se possível, de uma das propriedades de destino. Se o tipo for desconhecido, de definida como PT_UNSPECIFIED. Se o tipo e o identificador são desconhecidos, localize essas informações chamando [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** retorna uma matriz de marca de propriedade com todas as propriedades com suporte do objeto. Se apenas um nome de propriedade estiver disponível, chame [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para acessar o identificador associado. 
    
3. Chame [IMAPIProp::GetProps](imapiprop-getprops.md) para abrir a propriedade ou as propriedades. 
    
O **método OpenProperty** é usado para abrir propriedades maiores que exigem uma interface alternativa, como **IStream** ou [IMAPITable,](imapitableiunknown.md) para acesso. **OpenProperty** é geralmente usado para abrir propriedades de objetos, binários e cadeias de caracteres grandes e somente pode abrir uma propriedade de cada vez. Os chamadores passam o identificador da interface adicional que é necessária como um dos parâmetros de entrada. 
  
Alguns dos usos comuns de **OpenProperty** incluem abrir **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade que mantém o corpo de uma mensagem baseada em texto, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), a propriedade que contém um objeto OLE ou anexo de mensagem **e PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), a propriedade que contém uma pasta ou tabela de conteúdo do contêiner do livro de endereços. 
  
Dependendo da propriedade, uma interface diferente é solicitada do **OpenProperty**. **IStream**, uma interface que permite que os dados de propriedade sejam lidos e gravados como um fluxo de bytes, é normalmente usado para acessar PR_BODY **.** [IMessage](imessageimapiprop.md) ou **IStream** podem ser usados para **acessar** PR_ATTACH_DATA_OBJ . Anexos de mensagem incorporados que são mensagens padrão usam **IMessage,** enquanto as mensagens no formato TNEF usam **IStream**. Como **PR_CONTAINER_CONTENTS** é um objeto de tabela, ele é acessado com [IMAPITable](imapitableiunknown.md).
  
 **Para recuperar a propriedade de PR_ATTACH_DATA_BIN anexo**
  
1. Chame a [função OpenStreamOnFile](openstreamonfile.md) para abrir um fluxo para o arquivo. 
    
2. Chame o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para recuperar a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) com a interface **IStream.** De definir os sinalizadores MAPI_MODIFY e MAPI_CREATE de configuração. 
    
3. Aloce uma **estrutura STATSTG** e passe-a em uma chamada para o método **IStream::Stat** do fluxo de arquivos para determinar seu tamanho. Outra maneira de determinar o tamanho do fluxo é chamar **IStream::Seek** com o sinalizador STREAM_SEEK_END. 
    
4. Chame o método **IStream::CopyTo** do fluxo para copiar os dados do fluxo do arquivo para o fluxo de anexo. 
    
5. Quando a operação de cópia for concluída, libere ambos os fluxos chamando seus métodos **IUnknown::Release.** 
    
Quando **o IStream** é usado para o acesso à propriedade, alguns provedores de serviços enviam automaticamente o tamanho da propriedade de volta com o fluxo. Chamar **OpenProperty** com o sinalizador MAPI_DEFERRED_ERRORS pode atrasar a abertura da propriedade e o retorno do tamanho do fluxo. Se **IStream::Stat** for chamado para recuperar esse tamanho após **OpenProperty** com o sinalizador MAPI_DEFERRED_ERRORS definido, o desempenho será afetado porque essa sequência de chamadas força uma chamada de procedimento remoto extra. Para evitar o desempenho atingido, os clientes podem chamar qualquer método MAPI entre as chamadas para **OpenProperty** e **Stat**.
  
A [função HrGetOneProp,](hrgetoneprop.md) como **OpenProperty,** abre uma propriedade por vez. **HrGetOneProp** só deve ser usado quando o objeto de destino existe no computador local. Quando o objeto de destino não está disponível localmente, o uso de **HrGetOneProp** repetidamente pode resultar em várias chamadas de procedimento remoto e uma degradação do desempenho. 
  
Os chamadores que precisam de várias propriedades podem chamar **HrGetOneProp** ou **OpenProperty** em um loop ou fazer uma chamada para **GetProps**. Chamar **GetProps** uma vez é mais eficiente. 
  
> [!NOTE]
> As propriedades seguras não estão disponíveis automaticamente com outras propriedades em uma chamada **GetProps**, **HrGetOneProp** ou **GetPropList.** As propriedades seguras devem ser explicitamente solicitadas usando seus identificadores de propriedade. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

