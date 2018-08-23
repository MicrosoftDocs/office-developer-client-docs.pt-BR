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
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577412"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte a administração de perfis. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Expostos pelo:  <br/> |Objeto de administração de perfil  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IProfAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com um objeto de administração do perfil.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Fornece acesso à tabela de perfis, uma tabela que contém informações sobre todos os perfis disponíveis.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Cria um novo perfil.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Exclui um perfil.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Obsoleto. Altera a senha de um perfil.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Copia um perfil.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Atribui um novo nome a um perfil.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Define ou limpa o perfil padrão de um cliente.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Fornece acesso a um objeto de administração do serviço de mensagem para aplicar alterações para os serviços de mensagem em um perfil.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

