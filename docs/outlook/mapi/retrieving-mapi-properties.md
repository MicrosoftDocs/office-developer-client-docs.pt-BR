---
title: Recuperar as propriedades MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: 1404239a54f9b8991099a66831e3364d9a683d1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566331"
---
# <a name="retrieving-mapi-properties"></a>Recuperar as propriedades MAPI

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um cliente ou serviço provedor recupera uma propriedade de um objeto, o objeto disponibiliza identificador, tipo e o valor da propriedade. 
  
Clientes e provedores de serviços podem recuperar propriedades de um objeto chamando um destes procedimentos:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
O método **GetProps** é usado para recuperar uma ou mais propriedades que não precisam de uma interface especializada ou alternativa para acesso. Isso significa que as propriedades disponíveis com **GetProps** são pequenas, como números inteiros e valores booleanos. 
  
 **Para recuperar as várias propriedades**
  
1. Aloca uma estrutura [SPropTagArray](sproptagarray.md) grande o suficiente para armazenar o número de propriedades a ser recuperado. 
    
2. Defina o membro **cValues** da estrutura **SPropTagArray** como o número de propriedades a ser recuperada e definir cada membro **aulPropTag** para o identificador e tipo, se possível, de uma das propriedades de destino. Se o tipo for desconhecido, você deve defini-la como PT_UNSPECIFIED. Se o tipo e o identificador desconhecidos, localize essa informação chamando [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** retorna uma matriz de marca de propriedade com todas as propriedades do objeto com suporte. Se houver apenas um nome de propriedade disponível, chame [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para acessar o identificador associado. 
    
3. Chame [IMAPIProp::GetProps](imapiprop-getprops.md) para abrir a propriedade ou propriedades. 
    
O método **OpenProperty** é usado para abrir propriedades maiores que requerem uma interface alternativa como **IStream** ou [IMAPITable](imapitableiunknown.md) para acesso. **OpenProperty** geralmente é utilizado para abrir a cadeia de caracteres grandes, binário e propriedades do objeto e pode somente abrir uma propriedade por vez. Os chamadores passam o identificador da interface adicional que é necessário como um dos parâmetros de entrada. 
  
Alguns dos usos comuns do **OpenProperty** incluem a abertura de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade que contém o corpo da mensagem com base em texto, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), a propriedade que retém uma Objeto OLE ou mensagem anexo e **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), a propriedade que contém uma tabela de conteúdo de contêiner de catálogo de endereço ou de pasta. 
  
Dependendo da propriedade, uma interface diferente é solicitada da **OpenProperty**. **IStream**, uma interface que permite que os dados de propriedade ser lido e gravado como um fluxo de bytes, geralmente é utilizado para acessar **PR_BODY**. [IMessage](imessageimapiprop.md) ou **IStream** pode ser usado para acessar **PR_ATTACH_DATA_OBJ**. Anexos de mensagens inseridas que são mensagens standard usam **IMessage** enquanto as mensagens no formato TNEF usam **IStream**. Como **PR_CONTAINER_CONTENTS** é um objeto table, ele é acessado com [IMAPITable](imapitableiunknown.md).
  
 **Para recuperar a propriedade PR_ATTACH_DATA_BIN do anexo**
  
1. Chame a função [OpenStreamOnFile](openstreamonfile.md) para abrir um fluxo para o arquivo. 
    
2. Chame o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da mensagem para recuperar a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) com a interface **IStream** . Defina os sinalizadores de MAPI_MODIFY e MAPI_CREATE. 
    
3. Alocar uma estrutura **STATSTG** e passe-o em uma chamada ao método de **IStream::Stat** do fluxo de arquivos para determinar seu tamanho. Outra maneira de determinar o tamanho do fluxo é chamar **IStream::Seek** com o sinalizador STREAM_SEEK_END. 
    
4. Chame o método de **IStream::CopyTo** do fluxo para copiar os dados do fluxo do arquivo para o fluxo de anexos. 
    
5. Quando a operação de cópia é concluída, release ambos os fluxos chamando os métodos **IUnknown:: Release** . 
    
Quando **IStream** é usada para acesso à propriedade, alguns provedores de serviços enviam automaticamente o tamanho da propriedade volta com o fluxo. Sinalizador chamar **OpenProperty** com o MAPI_DEFERRED_ERRORS poderá atrasar a abertura da propriedade e o retorno do tamanho do fluxo. Se **IStream::Stat** é chamado para recuperar esse tamanho após **OpenProperty** com o MAPI_DEFERRED_ERRORS o sinalizador será definido, o desempenho será afetado porque esta sequência de chamadas força uma chamada de procedimento remoto extra. Para evitar o impacto no desempenho, os clientes podem chamar qualquer método MAPI entre as chamadas para **OpenProperty** e **Stat**.
  
A função [HrGetOneProp](hrgetoneprop.md) , como **OpenProperty**, abre uma propriedade por vez. **HrGetOneProp** deve ser usado apenas quando o objeto de destino não existe na máquina local. Quando o objeto de destino não estiver disponível localmente, usar **HrGetOneProp** repetidamente pode resultar em várias chamadas de procedimento remoto e uma diminuição do desempenho. 
  
Os chamadores que precisam de várias propriedades podem chamar **HrGetOneProp** ou **OpenProperty** em um loop ou fazer uma chamada para **GetProps**. Chamar **GetProps** uma vez é mais eficiente. 
  
> [!NOTE]
> Propriedades protegidas não ficam disponíveis automaticamente com outras propriedades em uma chamada **GetProps**, **HrGetOneProp**ou **GetPropList** . Propriedades protegidas devem ser explicitamente solicitadas usando seus identificadores de propriedade. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

