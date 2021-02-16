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
  
Contém uma máscara de bits de sinalizadores que regem o comportamento de um controle usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Identificador:  <br/> |0x3F00  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabela de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos sinalizadores a seguir podem ser definidos para essa propriedade:
  
DT_ACCEPT_DBCS 
  
> O controle pode ter Double-Byte caracteres DBCS (Conjunto de Caracteres). Esse sinalizador é usado com controles de edição. Ele permite conjuntos de caracteres de vários byte.
    
DT_EDITABLE 
  
> O controle pode ser editado; o valor associado ao controle pode ser alterado. Quando esse sinalizador não está definido, o controle é somente leitura. Esse valor é ignorado nos controles rótulo, caixa de grupo, botão de push padrão, caixa de listagem de valores múltiplos e controles de caixa de listagem.
    
DT_MULTILINE 
  
> O controle de edição pode conter várias linhas. Isso significa que um caractere de retorno pode ser inserido dentro do controle. Esse sinalizador é válido somente para controles de edição.
    
DT_PASSWORD_EDIT 
  
> Aplica-se a controles de edição. O controle de edição é tratado como uma senha. O valor é exibido usando asteriscos em vez de exibir os caracteres reais inseridos.
    
DT_REQUIRED 
  
> Se o controle permitir alterações (DT_EDITABLE), ele deverá ter um valor antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ser chamado. 
    
DT_SET_IMMEDIATE 
  
> Habilita a configuração imediata de um valor; assim que um valor no controle é muda, MAPI chama o método **SetProps** para a propriedade associada a esse controle. Quando esse sinalizador não está definido, os valores são definidos quando a caixa de diálogo é descartada. 
    
DT_SET_SELECTION 
  
> Quando uma seleção é feita dentro da caixa de listagem, a coluna de índice dessa caixa de listagem é definida como uma propriedade. Sempre usado com DT_SET_IMMEDIATE.
    
Essa propriedade é armazenada no membro ulCtlFlags da estrutura [DTCTL de um](dtctl.md) controle. A maioria dos sinalizadores de controle se aplica a todos os controles que permitem a entrada do usuário; alguns se aplicam somente ao controle de edição. Os controles que não permitem a entrada do usuário, como um botão ou um rótulo, são definidos como 0 para seus sinalizadores de controle. 
  
Muitos dos valores de sinalizador são autoexplicativos. Por exemplo, quando DT_REQUIRED definido para um controle, ele deve conter um valor antes que a caixa de diálogo tenha permissão para ser descartada. O provedor de serviços pode fornecer um valor por meio de sua implementação **IMAPIProp** ou o usuário pode inserir um. DT_EDITABLE indica que o valor do controle pode ser modificado. DT_MULTILINE permite que o valor de um controle de edição se estendo por várias linhas. 
  
Alguns sinalizadores de controle não são tão óbvios em seu significado. Quando um controle define o DT_SET_IMMEDIATE, qualquer alteração em seu valor será efetivada assim que o usuário for para um novo controle. MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property. Isso é diferente do comportamento padrão, que é adiar a ação de ter alterações nos valores de controle até que o usuário selecione o botão **OK** ou descarte a caixa de diálogo. O DT_SET_IMMEDIATE sinalizador geralmente é usado em combinação com as notificações da tabela de exibição. 
  
A tabela a seguir lista os tipos de controles e todos os valores de sinalizador que podem ser definidos para cada tipo.
  
|**Control**|**Valores válidos para essa propriedade**|
|:-----|:-----|
|Botão  <br/> |Deve ser zero  <br/> |
|Caixa de seleção  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Caixa de combinação  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de listagem drop-down  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Editar  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Caixa de grupo  <br/> |Deve ser zero  <br/> |
|Rótulo  <br/> |Deve ser zero  <br/> |
|Caixa de listagem  <br/> |Deve ser zero  <br/> |
|Caixa de listagem de valores múltiplos  <br/> |Deve ser zero  <br/> |
|Caixa de listagem de vários valores  <br/> |Deve ser zero  <br/> |
|Página com guias  <br/> |Deve ser zero  <br/> |
|Botão de rádio  <br/> |Deve ser zero  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

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

