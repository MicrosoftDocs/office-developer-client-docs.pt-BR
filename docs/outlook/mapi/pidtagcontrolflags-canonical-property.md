---
title: Propriedade canônica PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430879"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Propriedade canônica PidTagControlFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores que regem o comportamento de um controle usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos seguintes sinalizadores podem ser definidos para esta propriedade:
  
DT_ACCEPT_DBCS 
  
> O controle pode ter caracteres de conjunto de caracteres de byte duplo (DBCS). Este sinalizador é usado com controles de edição. Ele permite conjuntos de caracteres de vários bytes.
    
DT_EDITABLE 
  
> O controle pode ser editado; o valor associado ao controle pode ser alterado. Quando esse sinalizador não é definido, o controle é somente leitura. Esse valor é ignorado em rótulo, caixa de grupo, botão de ação padrão, caixa de listagem suspensa de vários valores e controles de caixa de listagem.
    
DT_MULTILINE 
  
> O controle de edição pode conter várias linhas. Isso significa que um caractere de retorno pode ser inserido dentro do controle. Este sinalizador é válido apenas para controles de edição.
    
DT_PASSWORD_EDIT 
  
> Aplica-se a controles de edição. O controle de edição é tratado como uma senha. O valor é exibido usando asteriscos em vez de ecoar os caracteres reais inseridos.
    
DT_REQUIRED 
  
> Se o controle permitir alterações (DT_EDITABLE), ele deverá ter um valor antes que [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) seja chamado. 
    
DT_SET_IMMEDIATE 
  
> Habilita a configuração imediata de um valor; assim que um valor no controle é alterado, o MAPI chama o **** método SetProps para a propriedade associada a esse controle. Quando esse sinalizador não é definido, os valores são definidos quando a caixa de diálogo é descartada. 
    
DT_SET_SELECTION 
  
> Quando uma seleção é feita dentro da caixa de listagem, a coluna de índice dessa caixa de listagem é definida como uma propriedade. Sempre usado com DT_SET_IMMEDIATE.
    
Essa propriedade é armazenada no membro ulCtlFlags da estrutura [DTCTL](dtctl.md) de um controle. A maioria dos sinalizadores de controle se aplicam a todos os controles que permitem a entrada do usuário; algumas aplicam-se apenas ao controle de edição. Controles que não permitem a entrada do usuário, como um botão ou um rótulo, definem 0 para seus sinalizadores de controle. 
  
Muitos dos valores de sinalizador são auto-explicativos. Por exemplo, quando DT_REQUIRED é definido para um controle, ele deve conter um valor antes que a caixa de diálogo tenha permissão para ser descartada. O provedor de serviços pode fornecer um valor através de sua implementação de **IMAPIProp** ou o usuário pode inserir um. DT_EDITABLE indica que o valor do controle pode ser modificado. DT_MULTILINE permite que o valor de um controle de edição estenda várias linhas. 
  
Alguns sinalizadores de controle não são tão óbvios no significado. Quando um controle define o sinalizador DT_SET_IMMEDIATE, todas as alterações feitas em seu valor são afetadas assim que o usuário move para um novo controle. MAPI faz uma única chamada para o método [IMAPIProp::](imapiprop-setprops.md) SetProps da interface de propriedade para a propriedade do controle. Isso é diferente do comportamento padrão, que é adiar a necessidade de alterações nos valores de controle até que o usuário selecione o botão **OK** ou disperca a caixa de diálogo. O sinalizador DT_SET_IMMEDIATE é geralmente usado em combinação com notificações de tabela de exibição. 
  
A tabela a seguir lista os tipos de controles e todos os valores de sinalizador que podem ser definidos para cada tipo.
  
|**Control**|**Valores válidos para essa propriedade**|
|:-----|:-----|
|Botão  <br/> |Deve ser zero  <br/> |
|Caixa de seleção  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Caixa de combinação  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de listagem suspensa  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Edit  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de grupo  <br/> |Deve ser zero  <br/> |
|Rótulo  <br/> |Deve ser zero  <br/> |
|Caixa de listagem  <br/> |Deve ser zero  <br/> |
|Caixa de listagem suspensa de múltiplos valores  <br/> |Deve ser zero  <br/> |
|Caixa de listagem de vários valores  <br/> |Deve ser zero  <br/> |
|Página com guias  <br/> |Deve ser zero  <br/> |
|Botão de opção  <br/> |Deve ser zero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

