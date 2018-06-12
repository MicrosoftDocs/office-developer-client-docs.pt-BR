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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fa439d0a6fa59bac787f09c3f894a750948a0a3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767033"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo: IMAPIProp

  
  
**Aplica-se a**: Outlook 
  
Aplicativos cliente de fornece acesso às propriedades específicas para a definição do formulário. Mantendo as informações do formulário em um objeto separado, o provedor de bibliotecas de formulário pode descrever um formulário para um cliente sem ativando o formulário.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Expostos pelo:  <br/> |Objetos de informações de formulário  <br/> |
|Implementada por:  <br/> |Provedores de biblioteca de formulário  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIFormInfo  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPIFORMINFO  <br/> |
|Modelo de transação:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Retorna um ponteiro para o conjunto completo de propriedades que usa um formulário.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Retorna um ponteiro para o conjunto completo de verbos que usa um formulário.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Um ícone de uma propriedade de ícone de um formulário se baseia.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Salva uma descrição de um determinado formulário em um arquivo de configuração.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Retorna um ponteiro para o contêiner de formulário na qual um determinado formulário está instalado.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Ao contrário da maioria das interfaces definidas no arquivo de cabeçalho MapiForm.h, **IMAPIFormInfo** herda da interface [IMAPIProp](imapipropiunknown.md) , pois ele exporta a maioria das informações do formulário por meio de chamadas para o método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

