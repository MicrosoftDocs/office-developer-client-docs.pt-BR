---
title: Propriedade canônica PidTagAdditionalRenEntryIdsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768923"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propriedade canônica PidTagAdditionalRenEntryIdsEx

  
  
**Aplica-se a**: Outlook 
  
Contém os IDs de entradas de pasta especial para um objeto de repositório. Cada entrada nessa propriedade de valores múltiplos pode ser mapeada para um ou mais identificações de entrada, ou seja, há uma relação um-para-muitos entre uma entrada e suas identificações de entrada associada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificador:  <br/> |0x36D9  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for usada, ele contém uma matriz de blocos que especifica a entrada de IDs para as pastas. Os blocos de seguem o formato especificado pelo quatro tabelas a seguir.
  
**Bloco de PersistData**

|**Name**|**Type**|**Size**|**Descrição**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Digite o valor do identificador para essa entrada **PersistData** . Consulte a tabela "PersistBlockType valores" na lista de valores válidos.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Tamanho, em bytes, do campo **DataElements** .  <br/> |
|**DataElements** <br/> |matriz de blocos de **PersistElement**  <br/> |variável  <br/> |Indica quantas entradas **PersistElement** existem para o repositório. Consulte a tabela "PersistElement Block" para o formato desta estrutura.  <br/> |
   
**Valores de PersistBlockType**

|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indica que não há mais blocos **PersistData** serão processados.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indica que este bloco contém dados para a pasta de assinaturas RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indica que este bloco contém dados para a pasta de processamento de email controlado.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indica que este bloco contém dados da pasta de pesquisa de tarefas pendentes.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indica que este bloco contém dados para a pasta de configurações de ação de conversa.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Esse valor é reservado.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indica que este bloco contém dados para a pasta Contatos sugeridos.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indica que este bloco contém dados da pasta de pesquisa de contatos.  <br/> Usado somente pelo Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indica que este bloco contém dados para a pasta de listas de contatos de mensagens instantâneas (IM). A pasta referenciada contém listas de distribuição pessoal (PDLs) que representam cada grupo dentro da lista de contatos de mensagens Instantâneas.  <br/> Usado pelo Outlook e Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indica que este bloco contém dados para a pasta de contatos de mensagens Instantâneas. A pasta referenciada contém os contatos individuais referenciados pelos grupos da lista de contatos de mensagens Instantâneas.  <br/> Usado pelo Outlook e Exchange.  <br/> |
   
Se o valor de **PersistBlockType** não for uma daquelas definidas aqui, o bloco de **PersistData** será ignorado e o processamento continua até que um PERSIST_SENTINEL **PersistID** é processada ou o fim do fluxo é atingido. 
  
**PersistElementBlock**

|**Name**|**Type**|**Size**|**Descrição**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Especifica o valor do identificador de tipo para este bloco **PersistElement** . Consulte a tabela "PersistElementType valores" para obter uma lista de valores válidos.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Especifica o tamanho, em bytes, do campo **ElementData** .  <br/> |
|**ElementData** <br/> |matriz de dados binários  <br/> |variável  <br/> |Contém os dados para este **PersistID** + **ElementID** par.  <br/> |
   
**Valores de PersistElementType**

|**Name**|**Valor**|**Valor da ElementDataSize**|**Descrição**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indica que o campo de **ElementData** deste bloco contém um valor de cabeçalho de DWORD. Como esse valor é interpretado depende do tipo de **PersistID** do bloco.  <br/> Para todos os tipos de **PersistID** especificados no [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), esse valor é zero.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variável  <br/> |Indica que este bloco contém a **EntryID** da pasta especificada pelo **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indica que não há mais blocos **PersistElement** serão processados.  <br/> |
   
Se o valor de **PersistElementType** não for uma daquelas definidas aqui, o bloco de **PersistElement** será ignorado e o processamento continua até que um ELEMENT_SENTINEL **ElementID** é processada ou o fim do fluxo é atingido. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica e marca mensagens de email que foram projetadas para fazer com que os destinatários a divulgação de informações confidenciais (por exemplo, senhas e outras informações pessoais) para uma fonte não confiável.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

