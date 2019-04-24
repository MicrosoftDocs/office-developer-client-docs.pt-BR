---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309545"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso à tabela de perfil, uma tabela que contém informações sobre todos os perfis disponíveis.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Sempre nulo.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de perfis.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de perfil foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::** getprofiletable fornece acesso à tabela de perfis, que contém uma linha para cada perfil disponível. Há apenas duas colunas em cada linha: o nome de exibição do perfil e um sinalizador que indica se o perfil é o padrão. 
  
Os perfis excluídos ou que estão em uso, mas que foram marcados para exclusão, não estão incluídos na tabela de perfis. A tabela de perfil é estática; adições e exclusões subsequentes de perfis não são refletidas na tabela. 
  
Se não existir nenhum perfil **** , getprofiletable retornará uma tabela com zero linhas. 
  
Para obter mais informações sobre a tabela de perfil, consulte [tabelas de perfil](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnShowProfiles  <br/> |MFCMAPI usa o método **IProfAdmin::** getprofiletable para fazer com que a tabela de perfil seja exibida em uma nova caixa de diálogo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

