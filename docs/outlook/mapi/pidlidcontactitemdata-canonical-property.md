---
title: Propriedade canônica PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f363b0a756a2cf4c7e37854cab0ddc4a46a0754d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582655"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propriedade canônica PidLidContactItemData

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Usado para exibir as informações de contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidContactItemData  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008007  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se presente, a propriedade deve ter seis entradas, cada um correspondendo a um campo visível na interface do usuário do aplicativo.
  
|**Baseado em um índice para a propriedade de valores múltiplos**|**O valor deve ser um dos seguintes**|**Descrição**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |O aplicativo deve exibir endereço residencial do contato.  <br/> |
|1  <br/> |0x00000002 ou 0x00000000  <br/> |O aplicativo deve exibir comercial do contato.  <br/> |
|1  <br/> |0x00000003  <br/> |O aplicativo deve exibir o contato do outro endereço.  <br/> |
|2  <br/> |0x00008080  <br/> |O aplicativo deve exibir Email1.  <br/> |
|2  <br/> |0x00008090  <br/> |O aplicativo deve exibir Email2.  <br/> |
|2  <br/> |0x000080A0  <br/> |O aplicativo deve exibir Email3.  <br/> |
|3,4,5,6  <br/> |PropertyID de qualquer uma das propriedades telefônica ou de qualquer um dos números de fax que foram especificados em [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |O aplicativo deve exibir a propriedade correspondente.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

