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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358508"
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

Essa propriedade é um valor binário que identifica exclusivamente uma linha em um exibição de tabela. É uma coluna necessária na maioria das tabelas. Se uma linha estiver incluída em dois modo de exibição, haverá duas chaves de instância diferentes. A chave de instância de uma linha pode diferir sempre que a tabela for aberta, mas permanecerá constante enquanto a tabela estiver aberta. Linhas adicionadas enquanto uma tabela está em uso não reutilizar uma chave de instância que foi usada anteriormente. 
  
Use as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para correlacionar todas as linhas de uma expansão. Use **PR_INSTANCE_KEY** para localizar uma instância específica dentro da expansão. 
  
Quando uma propriedade de múltiplos valores é expandida em uma tabela, uma linha é criada para cada instância da expansão, ou seja, para cada valor dessa propriedade. Cada linha tem um valor exclusivo para a **propriedade PR_INSTANCE_KEY,** enquanto todas as outras colunas mantêm seus valores originais durante toda a expansão. 
  
Em uma classificação categorizada de uma tabela, linhas não correspondentes a dados reais podem ser adicionadas ao resultado da classificação. Cada linha, como todas as linhas em todas as tabelas, tem sua própria chave de instância exclusiva. 
  
 **PR_INSTANCE_KEY** também é usado em notificações de eventos de tabela. Os **membros propIndex** e **propPrior** da estrutura [TABLE_NOTIFICATION](table_notification.md) estruturas [SPropValue](spropvalue.md) que PR_INSTANCE_KEY **valores.** O **membro propIndex** indica a linha que foi adicionada ou alterada. O **membro propPrior** indica a linha antes da linha adicionada ou alterada (**PR_NULL** indica uma alteração na primeira linha). 
  
Esse valor não é copiado como parte da tabela de exibição. 
  
 **PR_INSTANCE_KEY** é uma [estrutura MAPIUID.](mapiuid.md) Todas as chaves de instância podem ser comparadas diretamente como valores binários. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

