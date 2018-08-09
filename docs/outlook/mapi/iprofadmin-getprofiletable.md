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
ms.openlocfilehash: c942bdbf27590dde04b84970e345f265bc645045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767631"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso à tabela de perfis, uma tabela que contém informações sobre todos os perfis disponíveis.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Sempre nulo.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de perfil.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de perfil foi recuperada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::GetProfileTable** fornece acesso à tabela de perfis, que contém uma linha para cada perfil disponível. Existem apenas duas colunas em cada linha: nome para exibição do perfil e um sinalizador que indica se o perfil é o padrão. 
  
Perfis que tenha sido excluída, ou que estão em uso, mas foram marcadas para exclusão, não são incluídos na tabela de perfil. A tabela de perfil é estática; subsequentes adições e exclusões de perfis não serão refletidas na tabela. 
  
Se nenhum perfil existir, **GetProfileTable** retorna uma tabela com zero linhas. 
  
Para obter mais informações sobre a tabela de perfil, consulte [As tabelas de perfil](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI usa o método **IProfAdmin::GetProfileTable** para obter a tabela de perfil para exibir em uma nova caixa de diálogo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

