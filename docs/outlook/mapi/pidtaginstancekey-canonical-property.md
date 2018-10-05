---
title: Propriedade canônica PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396985"
---
# <a name="pidtaginstancekey-canonical-property"></a>Propriedade canônica PidTagInstanceKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que identifica exclusivamente uma linha em uma tabela. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_INSTANCE_KEY  <br/> |
|Identificador:  <br/> |0x0FF6  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Table  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é um valor binário que identifica exclusivamente uma linha em um modo de exibição de tabela. É uma coluna obrigatória na maioria das tabelas. Se uma linha é incluída nos dois modos de exibição, existem duas chaves de instância diferente. A chave de instância de uma linha pode ser diferente a cada vez que a tabela é aberta, mas permanece constante enquanto a tabela é aberta. Linhas adicionadas enquanto uma tabela está em uso não reutilizam uma chave de instância que foi usada anteriormente. 
  
Use as propriedades de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) ou o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para correlacionar todas as linhas de uma expansão. Use **PR_INSTANCE_KEY** para localizar uma determinada instância dentro a expansão. 
  
Quando uma propriedade de valores múltiplos é expandida em uma tabela, uma linha é criada para cada instância da expansão, ou seja, para cada valor dessa propriedade. Cada linha tem um valor exclusivo para a propriedade **PR_INSTANCE_KEY** , enquanto todas as outras colunas mantêm seus valores originais em toda a expansão. 
  
Em uma classificação categorizada de uma tabela, linhas não correspondente à dados reais podem ser adicionadas ao resultado da classificação. Cada tal linha, como todas as linhas em todas as tabelas, tem sua própria chave de instância exclusivo. 
  
 **PR_INSTANCE_KEY** também é usado em notificações de eventos de tabela. Os membros **propIndex** e **propPrior** da estrutura [TABLE_NOTIFICATION](table_notification.md) são estruturas de [SPropValue](spropvalue.md) contendo os valores **PR_INSTANCE_KEY** . O membro **propIndex** indica a linha que foram adicionada ou alterada. O membro **propPrior** indica a linha antes da linha adicionada ou alterada (**PR_NULL** indica uma alteração à primeira linha). 
  
Este valor não é copiado como parte da tabela de exibição. 
  
 **PR_INSTANCE_KEY** é uma estrutura [MAPIUID](mapiuid.md) . Todas as chaves de instância podem ser comparadas diretamente como valores binários. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

