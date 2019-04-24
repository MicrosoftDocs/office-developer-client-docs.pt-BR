---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321634"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma interface [IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico. 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parâmetros

 _hfrmreg_
  
> no Uma enumeração HFRMREG que indica a biblioteca de formulários a ser aberta (ou seja, o contêiner de formulários a ser aberto). Uma enumeração HFRMREG é uma enumeração específica para um provedor de biblioteca de formulários. Os valores possíveis de HFRMREG incluem o seguinte:
    
HFRMREG_DEFAULT 
  
> Um contêiner de formulário conveniente.
    
HFRMREG_FOLDER 
  
> Um contêiner de pasta. 
    
HFRMREG_PERSONAL 
  
> O contêiner para o repositório de mensagens padrão. 
    
HFRMREG_LOCAL 
  
> Um contêiner de formulário local. 
    
 _lpUnk_
  
> no Um ponteiro para o objeto para o qual a interface é aberta. O parâmetro _lpUnk_ deve ser **NULL** , a menos que o valor do parâmetro _hfrmreg_ exija um ponteiro de objeto. 
    
 _lppfcnt_
  
> bota Um ponteiro para um ponteiro para o objeto contêiner Form retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_INTERFACE 
  
> O objeto apontado pelo _lpUnk_ não dá suporte à interface necessária. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: OpenFormContainer** para abrir uma interface **IMAPIFormContainer** para um contêiner de formulário específico. Essa interface pode ser usada para instalar formulários no e remover formulários de um contêiner de formulários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o valor em _hfrmreg_ for HFRMREG_FOLDER, o identificador de interface usado no _lpUnk_ deve ser não **nulo** e deve permitir [IUnknown::](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) chamadas de método de QueryInterface para uma interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
Para abrir o contêiner de formulário local, você deve usar uma chamada para o método **OpenFormContainer** ou a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; Você não pode usar o método [IMAPIFormMgr:: SelectFormContainer](imapiformmgr-selectformcontainer.md) para permitir que o usuário selecione o contêiner de formulário local. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp  <br/> |CMainDlg:: OnOpenFormContainer  <br/> |MFCMAPI usa o método **IMAPIFormMgr:: OpenFormContainer** para recuperar um contêiner de formulários, de forma que o conteúdo do contêiner possa ser renderizado.  <br/> |
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnOpenFormContainer  <br/> |MFCMAPI usa o método **IMAPIFormMgr:: OpenFormContainer** para recuperar um contêiner de formulário para uma pasta para que o conteúdo do contêiner possa ser renderizado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

