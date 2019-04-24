---
title: Implementar a interface IClassFactory para servidores de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310028"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementar a interface IClassFactory para servidores de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) é a interface OLE que os aplicativos cliente usam para criar novos objetos de formulário da classe de mensagens do seu servidor de formulários. A tabela a seguir lista os métodos **IClassFactory** que são necessários. 
  
|**Método**|**Descrição**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Cria um novo objeto Form.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Bloqueia o servidor de formulário na memória para que a sobrecarga de inicialização possa ser evitada quando vários objetos de formulário são criados.  <br/> |
   
Para todas as informações necessárias para implementar esses métodos, consulte a seção de serviços de objeto COM e ActiveX no SDK do Windows.
  
## <a name="see-also"></a>Confira também



[Gravando código de servidor de formulário](writing-form-server-code.md)

