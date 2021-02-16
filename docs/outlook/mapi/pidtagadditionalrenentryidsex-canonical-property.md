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
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335200"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propriedade canônica PidTagAdditionalRenEntryIdsEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém IDs de entrada de pasta especial para um objeto de armazenamento. Cada entrada nessa propriedade de vários valores pode ser mapeada para uma ou mais IDs de entrada, ou seja, há uma relação um-para-muitos entre uma entrada e suas IDs de entrada associadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificador:  <br/> |0x36D9  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for usada, ela conterá uma matriz de blocos que especifica as IDs de entrada das pastas. Os blocos seguem o formato especificado pelas quatro tabelas a seguir.
  
**Bloco PersistData**

|**Nome**|**Tipo**|**Tamanho**|**Descrição**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2   <br/> |Valor do identificador de tipo para essa **entrada PersistData.** Consulte a tabela "PersistBlockType Values" para ver a lista de valores válidos.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2   <br/> |Tamanho, em bytes, do **campo DataElements.**  <br/> |
|**DataElements** <br/> |matriz de **blocos PersistElement**  <br/> |variável  <br/> |Indica quantas entradas **PersistElement** existem para o armazenamento. Consulte a tabela "PersistElement Block" para o formato dessa estrutura.  <br/> |
   
**Valores persistBlockType**

|**Nome**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indica que não serão processados mais **blocos persistData.**  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indica que esse bloco contém dados para a pasta Assinaturas RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indica que esse bloco contém dados para a pasta De processamento de email rastreado.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indica que esse bloco contém dados para a pasta To-Do Pesquisa.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indica que esse bloco contém dados para a pasta Configurações de Ação de Conversa.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Esse valor é reservado.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indica que esse bloco contém dados para a pasta Contatos Sugeridos.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indica que esse bloco contém dados para a pasta Pesquisa de Contatos.  <br/> Usado somente pelo Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indica que esse bloco contém dados para a pasta Listas de Contatos de Mensagens Instantâneas (IM). A pasta referenciada contém PDLs (Listas de Distribuição Pessoal) que representam cada grupo dentro da lista de Contatos de IM.  <br/> Usado pelo Outlook e pelo Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indica que esse bloco contém dados para a pasta Contatos de IM. A pasta referenciada contém os contatos individuais referenciados pelos grupos de Lista de Contatos de Mensagens IM.  <br/> Usado pelo Outlook e pelo Exchange.  <br/> |
   
Se o valor **PersistBlockType** não for um dos definidos aqui, o bloco **PersistData** será ignorado e o processamento será continuado até que um PERSIST_SENTINEL **PersistID** seja processado ou o final do fluxo seja atingido. 
  
**PersistElementBlock**

|**Nome**|**Tipo**|**Tamanho**|**Descrição**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2   <br/> |Especifica o valor do identificador de tipo para esse **bloco PersistElement.** Consulte a tabela "PersistElementType Values" para ver uma lista de valores válidos.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2   <br/> |Especifica o tamanho, em bytes, do **campo ElementData.**  <br/> |
|**ElementData** <br/> |matriz de dados binários  <br/> |variável  <br/> |Contém os dados para esse par **PersistID**  +  **ElementID.**  <br/> |
   
**Valores de PersistElementType**

|**Nome**|**Valor**|**Valor de ElementDataSize**|**Descrição**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indica que o campo **ElementData** desse bloco contém um valor de header DWORD. A maneira como esse valor é interpretado depende do tipo **PersistID do** bloco.  <br/> Para todos **os tipos PersistID** especificados [em [MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), esse valor é zero.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variável  <br/> |Indica que esse bloco contém a **EntryID** da pasta especificada por **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indica que não serão processados mais **blocos PersistElement.**  <br/> |
   
Se o valor **PersistElementType** não for um dos definidos aqui, o bloco **PersistElement** será ignorado e o processamento será continuado até que uma ELEMENT_SENTINEL **ElementID** seja processada ou o final do fluxo seja atingido. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica e marca mensagens de email projetadas para ajudar os destinatários a divulgar informações confidenciais (como senhas e outras informações pessoais) para uma fonte não confiável.
    
### <a name="header-files"></a>Arquivos de header

Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

