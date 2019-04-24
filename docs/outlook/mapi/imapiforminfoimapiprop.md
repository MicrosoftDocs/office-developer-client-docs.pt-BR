---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321732"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece aos aplicativos cliente acesso a propriedades que são específicas para a definição de formulários. Ao manter as informações de formulário em um objeto separado, o provedor de biblioteca de formulários pode descrever um formulário para um cliente sem ativar o formulário.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Exposto por:  <br/> |Objetos de informações de formulário  <br/> |
|Implementado por:  <br/> |Provedores de biblioteca de formulários  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormInfo  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMINFO  <br/> |
|Modelo de transação:  <br/> |Não-Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Retorna um ponteiro para o conjunto completo de propriedades que um formulário usa.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Cria um ícone a partir de uma Propriedade Icon de um formulário.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Salva uma descrição de um formulário específico em um arquivo de configuração.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Retorna um ponteiro para o contêiner de formulários no qual um determinado formulário é instalado.  <br/> |
   
## <a name="remarks"></a>Comentários

Ao contrário da maioria das interfaces definidas no arquivo de cabeçalho MapiForm. h, o **IMAPIFormInfo** herda da interface [IMAPIProp](imapipropiunknown.md) , porque exporta a maioria das informações de formulário através de chamadas para o método [IMAPIProp::](imapiprop-getprops.md) GetProps. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

