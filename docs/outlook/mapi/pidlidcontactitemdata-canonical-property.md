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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319506"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propriedade canônica PidLidContactItemData

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Usado para exibir as informações de contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidContactItemData  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008007  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se presente, a propriedade deve ter seis entradas, cada uma correspondendo a um campo visível na interface do usuário do aplicativo.
  
|**Índice baseado em um na propriedade de vários valores**|**O valor deve ser um dos seguintes:**|**Descrição**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |O aplicativo deve exibir o endereço residencial do contato.  <br/> |
|1   <br/> |0x00000002 ou 0x00000000  <br/> |O aplicativo deve exibir o trabalho do contato.  <br/> |
|1   <br/> |0x00000003  <br/> |O aplicativo deve exibir o outro endereço do contato.  <br/> |
|2   <br/> |0x00008080  <br/> |O aplicativo deve exibir Email1.  <br/> |
|2   <br/> |0x00008090  <br/> |O aplicativo deve exibir Email2.  <br/> |
|2   <br/> |0x000080A0  <br/> |O aplicativo deve exibir Email3.  <br/> |
|3,4,5,6  <br/> |PropertyID de qualquer uma das propriedades de telefone ou qualquer um dos números de fax especificados em [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |O aplicativo deve exibir a propriedade correspondente.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

