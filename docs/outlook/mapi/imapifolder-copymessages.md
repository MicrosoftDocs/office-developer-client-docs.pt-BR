---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280124"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move uma ou mais mensagens.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMsgList_
  
> no Um ponteiro para uma matriz de [](entrylist.md) estruturas de ENTRYLIST que identificam a mensagem ou mensagens a serem copiadas ou movidas. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta de destino indicada pelo parâmetro _lpDestFolder_ . Passar resultados nulos no provedor de serviços retornando a interface de pasta padrão, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Os clientes devem passar NULL. Outros chamadores podem definir o parâmetro _lpInterface_ como IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> no Um ponteiro para a pasta aberta para receber as mensagens copiadas ou movidas.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. O parâmetro _ulUIParam_ é ignorado, a menos que o cliente defina o sinalizador MESSAGE_DIALOG no parâmetro _PARÂMETROULFLAGS_ e passe nulo no parâmetro _lpProgress_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é realizada. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Informa ao provedor de repositório de mensagens para retornar imediatamente o MAPI_E_DECLINE_COPY se ele implementar **IMAPIFolder:: CopyMessages** chamando o objeto support [IMAPISupport::D ocopyto](imapisupport-docopyto.md) ou [IMAPISupport::D método ocopyprops](imapisupport-docopyprops.md) . 
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso à medida que a operação prossegue.
    
MESSAGE_MOVE 
  
> A mensagem ou as mensagens devem ser movidas em vez de copiadas. Se MESSAGE_MOVE não for definido, as mensagens serão copiadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem ou mensagens foram copiadas ou movidas com êxito.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implementa esse método chamando um método de objeto support e o chamador passou o sinalizador MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as entradas foram copiadas ou movidas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: CopyMessages** copia ou move mensagens para outra pasta. 
  
As mensagens abertas com permissão de leitura/gravação podem ser movidas ou copiadas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você estiver copiando mensagens para outro repositório de mensagens sem usar o método [IMAPISupport:: CopyMessages](imapisupport-copymessages.md) , primeiro você deve chamar [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) com o sinalizador GENERATE_RECEIPT_ONLY definido. O repositório de mensagens de recebimento não é responsável por gerar relatórios de leitura para as mensagens copiadas ou movidas. Se você estiver chamando **IMAPISupport:: CopyMessages** para implementar **IMAPIFolder:: CopyMessages**, não chame **SetReadFlags**; O MAPI o chamará. 
  
Sua implementação pode mover ou copiar as mensagens em qualquer ordem e gerar relatórios de status de leitura em qualquer ordem. Ou seja, você pode concluir a cópia de mensagens antes de gerar qualquer um dos relatórios de status de leitura ou enviar os relatórios antes que sua implementação inicie a operação de cópia. No enTanto, os relatórios de leitura devem ser enviados para que todas as mensagens sejam copiadas, independentemente da cópia ter sido bem-sucedida.
  
Quando a operação de cópia ou movimentação envolve mais de uma mensagem, execute a operação o mais completo possível. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.
  
Tente manter os identificadores de entrada nas operações de movimentação ou cópia. Você também deve preservar os identificadores de entrada, embora não seja necessário.
  
Enviar notificações quando você mover ou copiar mensagens para que os clientes sejam Forewarned que suas chamadas para as mensagens de [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) podem falhar. 
  
Não inclua o status de uma mensagem na operação de cópia ou movimentação. Mover ou copiar um status de mensagem afeta muito o desempenho.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use **IMAPIFolder:: CopyMessages** para preencher as pastas de resultados de pesquisa, onde as mensagens são agrupadas com frequência pela pasta pai. 
  
Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor retornado**|
|:-----|:-----|
|**IMAPIFolder:: CopyMessages** copiou ou moveu com êxito todas as mensagens.  <br/> |S_OK  <br/> |
|**IMAPIFolder:: CopyMessages** não pôde copiar ou mover com êxito todas as mensagens.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder:: CopyMessages** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Quando o **IMAPIFolder:: CopyMessages** não consegue concluir, não presuma que nenhum trabalho foi realizado. **IMAPIFolder:: CopyMessages** pode ser capaz de copiar ou mover uma ou mais mensagens antes de encontrar o erro. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

