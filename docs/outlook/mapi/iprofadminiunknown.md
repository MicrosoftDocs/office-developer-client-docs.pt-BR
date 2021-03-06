---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434113"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte à administração de perfis. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Exposto por:  <br/> |Objeto de administração de perfil  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
|Identificador de interface:  <br/> |IID_IProfAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu em um objeto de administração de perfil.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Fornece acesso à tabela de perfil, uma tabela que contém informações sobre todos os perfis disponíveis.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Cria um novo perfil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Exclui um perfil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Depreciado. Altera a senha de um perfil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copia um perfil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Atribui um novo nome a um perfil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Define ou limpa o perfil padrão de um cliente.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Fornece acesso a um objeto de administração do serviço de mensagens para fazer alterações nos serviços de mensagem em um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

