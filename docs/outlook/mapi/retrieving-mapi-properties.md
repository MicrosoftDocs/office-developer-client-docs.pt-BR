---
title: Recuperando propriedades MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328641"
---
# <a name="retrieving-mapi-properties"></a>Recuperando propriedades MAPI

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um cliente ou provedor de serviços recupera uma propriedade de um objeto, o objeto torna disponível o valor, tipo e identificador da propriedade. 
  
Os clientes e provedores de serviço podem recuperar as propriedades de um objeto chamando um dos seguintes:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
O **** método GetProps é usado para recuperar uma ou mais propriedades que não precisam de uma interface especializada ou alternativa para o Access. Isso implica que as propriedades disponíveis com **** GetProps são pequenas, como inteiros e valores booleanos. 
  
 **Para recuperar várias propriedades**
  
1. Aloque uma estrutura [SPropTagArray](sproptagarray.md) grande o suficiente para armazenar o número de propriedades a serem recuperadas. 
    
2. Defina o membro **cValues** da estrutura **SPropTagArray** para o número de propriedades a serem recuperadas e defina cada membro do **aulPropTag** como o identificador e o tipo, se possível, de uma das propriedades de destino. Se o tipo for desconhecido, defina-o como PT_UNSPECIFIED. Se o tipo e o identificador forem desconhecidos, localize essas informações chamando [IMAPIProp::](imapiprop-getproplist.md)getproplist. **** Getproplist retorna uma matriz de marca de propriedade com todas as propriedades com suporte do objeto. Se apenas um nome de propriedade estiver disponível, chame [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para acessar o identificador associado. 
    
3. Chame [IMAPIProp::](imapiprop-getprops.md) GetProps para abrir a propriedade ou propriedades. 
    
O **** método OpenProperty é usado para abrir Propriedades maiores que exigem uma interface alternativa como **IStream** ou IMAPITable para o Access. [](imapitableiunknown.md) **OpenProperty** normalmente é usado para abrir as propriedades de cadeia de caracteres, binária e de objeto grande e só pode abrir uma propriedade por vez. Os chamadores passam no identificador da interface adicional que é necessária como um dos parâmetros de entrada. 
  
Alguns dos usos comuns de **OpenProperty** incluem a abertura de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), a propriedade que contém o corpo de uma mensagem baseada em texto, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), a propriedade que contém um Objeto OLE ou anexo de mensagem, e **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), a propriedade que contém uma tabela de conteúdo de contêiner de catálogo de endereços ou pasta. 
  
Dependendo da propriedade, uma interface diferente é solicitada de **OpenProperty**. **IStream**, uma interface que permite que os dados de propriedade sejam lidos e gravados como um fluxo de bytes, geralmente é usada para acessar o **PR_BODY**. [IMessage](imessageimapiprop.md) ou **IStream** podem ser usados para acessar o **PR_ATTACH_DATA_OBJ**. Anexos de mensagens incorporadas que são mensagens padrão usam **IMessage** enquanto as mensagens no formato TNEF usam **IStream**. Como **PR_CONTAINER_CONTENTS** é um objeto Table, ele é acessado com IMAPITable. [](imapitableiunknown.md)
  
 **Para recuperar a propriedade PR_ATTACH_DATA_BIN de um anexo**
  
1. Chame a função [OpenStreamOnFile](openstreamonfile.md) para abrir um Stream para o arquivo. 
    
2. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) da mensagem para recuperar a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) com a interface **IStream** . Defina os sinalizadores MAPI_MODIFY e MAPI_CREATE. 
    
3. Aloque uma estrutura **STATSTG** e passe-a em uma chamada para o método **IStream:: stat** do fluxo de arquivos para determinar seu tamanho. Outra maneira de determinar o tamanho do fluxo é chamar **IStream:: Seek** com o sinalizador STREAM_SEEK_END. 
    
4. Chame o método **IStream:: CopyTo** do Stream para copiar os dados do Stream do arquivo no Stream de anexo. 
    
5. Quando a operação de cópia for concluída, libere os fluxos chamando seus métodos **IUnknown:: Release** . 
    
Quando **IStream** é usado para acesso de propriedade, alguns provedores de serviços enviam automaticamente o tamanho da propriedade de volta com o Stream. Chamar **OpenProperty** com o sinalizador MAPI_DEFERRED_ERRORS pode atrasar a abertura da propriedade e o retorno do tamanho do Stream. Se **IStream:: stat** for chamado para recuperar esse tamanho após **OpenProperty** com o sinalizador MAPI_DEFERRED_ERRORS definido, o desempenho será afetado porque essa sequência de chamadas força uma chamada de procedimento remoto extra. Para evitar o impacto do desempenho, os clientes podem chamar qualquer método MAPI entre as **** chamadas para OpenProperty e como **stat**.
  
A função [HrGetOneProp](hrgetoneprop.md) , como **OpenProperty**, abre uma propriedade por vez. **HrGetOneProp** deve ser usado somente quando o objeto target existe na máquina local. Quando o objeto de destino não está disponível localmente, o uso do **HrGetOneProp** repetidamente pode resultar em várias chamadas de procedimento remoto e em uma degradação de desempenho. 
  
Os chamadores que precisam de várias propriedades podem chamar **HrGetOneProp** ou **OpenProperty** em um loop ou fazer uma chamada para GetProps. **** Chamar **** GetProps uma vez é mais eficiente. 
  
> [!NOTE]
> As propriedades seguras não estão automaticamente disponíveis com outras propriedades em **** uma chamada GetProps, **HrGetOneProp**ou getproplist. **** As propriedades seguras devem ser explicitamente solicitadas usando seus identificadores de propriedade. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

