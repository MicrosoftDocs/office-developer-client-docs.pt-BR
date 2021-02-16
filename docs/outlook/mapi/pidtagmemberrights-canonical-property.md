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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342691"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propriedade canônica PidTagMemberRights

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um conjunto de bits que indica os direitos desse membro em uma pasta ou caixa de correio.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificador:  <br/> |0x6673  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Controle de Acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir direitos de um membro em uma pasta. Esses direitos podem ser exibidos e modificados. Os seguintes valores são direitos definidos para essa propriedade. 
  
readAny
  
> O membro pode ler todas as mensagens.
    
dasCreate
  
> O membro pode criar mensagens.
    
dasEditOwned
  
> O membro pode editar todas as mensagens pertencentes ao usuário.
    
adletadosDeleteOwned
  
> O membro pode excluir todas as mensagens pertencentes ao usuário.
    
daSeditAny
  
> O membro pode editar qualquer mensagem.
    
adlettasDeleteAny
  
> O membro pode excluir qualquer mensagem.
    
wesCreateSubfolder
  
> O membro pode criar subpastas para a pasta.
    
ownsOwner
  
> O membro tem todos os direitos anteriores na pasta.
    
adsContact
  
> O membro pode fazer com que seu nome apareça como contato na pasta.
    
daVisible
  
> O membro pode ver que a pasta existe.
    
rightsNone
  
> O membro não tem direitos na pasta.
    
rightsReadOnly
  
> O membro pode ler qualquer mensagem na pasta.
    
rightsReadWrite
  
> O membro pode ler e gravar em qualquer mensagem na pasta.
    
rightsAll
  
> O membro tem todos os direitos anteriores na pasta.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Lida com operações de pasta.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Lida com a recuperação de listas de permissões de pasta armazenadas no servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como representantes e interações com itens de mensagem e calendário quando eles agem em nome de outro usuário.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

