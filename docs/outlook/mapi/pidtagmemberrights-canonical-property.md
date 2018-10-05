---
title: Propriedade canônica PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397335"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propriedade canônica PidTagMemberRights

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um conjunto de bits que indicado os direitos deste membro em uma pasta ou caixa de correio.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificador:  <br/> |0x6673  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir os direitos de um membro em uma pasta. Esses direitos podem ser exibidos e modificados. Os seguintes valores são definidos para esta propriedade de direitos. 
  
frightsReadAny
  
> Membro pode ler todas as mensagens.
    
frightsCreate
  
> Membro pode criar mensagens.
    
frightsEditOwned
  
> Membro pode editar a todas as mensagens pertencentes ao usuário.
    
frightsDeleteOwned
  
> Membro pode excluir todas as mensagens pertencentes ao usuário.
    
frightsEditAny
  
> Membro pode editar qualquer mensagem.
    
frightsDeleteAny
  
> Membro pode excluir qualquer mensagem.
    
frightsCreateSubfolder
  
> Membro pode criar subpastas da pasta.
    
frightsOwner
  
> Membro tem todos os direitos anteriores na pasta.
    
frightsContact
  
> Membro pode ter seu nome aparecem como o contato na pasta.
    
frightsVisible
  
> Membro consegue ver a pasta existe.
    
rightsNone
  
> Membro não tem direitos na pasta.
    
rightsReadOnly
  
> Membro pode ler qualquer mensagem na pasta.
    
rightsReadWrite
  
> Membro pode ler e gravar a qualquer mensagem na pasta.
    
rightsAll
  
> Membro tem todos os direitos anteriores na pasta.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e configuração de caixas de correio conforme representantes e interações com itens de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

