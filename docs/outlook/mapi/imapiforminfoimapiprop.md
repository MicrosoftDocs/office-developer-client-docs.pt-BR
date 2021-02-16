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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417361"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece aos aplicativos cliente acesso a propriedades específicas da definição de formulário. Mantendo informações de formulário em um objeto separado, o provedor da biblioteca de formulário pode descrever um formulário para um cliente sem ativar o formulário.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Exposto por:  <br/> |Objetos de informações de formulário  <br/> |
|Implementado por:  <br/> |Provedores de biblioteca de formulário  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormInfo  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMINFO  <br/> |
|Modelo de transação:  <br/> |Não traduzido  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Retorna um ponteiro para o conjunto completo de propriedades que um formulário usa.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Cria um ícone a partir de uma propriedade de ícone de um formulário.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Salva uma descrição de um formulário específico em um arquivo de configuração.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Retorna um ponteiro para o contêiner de formulário no qual um formulário específico está instalado.  <br/> |
   
## <a name="remarks"></a>Comentários

Ao contrário da maioria das interfaces definidas no arquivo de cabeça MapiForm.h, **iMAPIFormInfo** herda da interface [IMAPIProp,](imapipropiunknown.md) porque ele exporta a maioria das informações de formulário por meio de chamadas para o método [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

