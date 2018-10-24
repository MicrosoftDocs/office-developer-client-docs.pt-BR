---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592567"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece a capacidade de recuperar e alterar o acesso para propriedades de um objeto. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Expostos pelo:  <br/> |Objeto de dados de propriedade  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIPropData  <br/> |
|Tipo de ponteiro:  <br/> |LPPROPDATA  <br/> |
|Modelo de transação:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Define o n�vel de acesso para o objeto.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Define o nível de acesso e o status de uma ou mais das propriedades do objeto.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Recupera o n�vel de acesso e o status de uma ou mais das propriedades do objeto.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IPropData::IMAPIProp** é implementada por MAPI e usada principalmente pelos provedores de serviços que acessam essa implementação chamando a função [CreateIProp](createiprop.md) . 
  
Para obter mais informações sobre níveis de acesso em objetos e propriedades, consulte [permissões para objetos e propriedades](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

