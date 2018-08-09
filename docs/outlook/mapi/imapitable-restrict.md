---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767347"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Aplica-se a**: Outlook 
  
Aplica um filtro a uma tabela, reduzindo a linha definida como apenas as linhas que correspondem aos critérios especificados.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpRestriction_
  
> [in] Ponteiro para uma estrutura de [SRestriction](srestriction.md) definindo as condições do filtro. Passar NULL no parâmetro _lpRestriction_ remove o filtro atual. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla o tempo da operação de restrição. Sinalizadores a seguir podem ser definidos:
    
TBL_ASYNC 
  
> Inicia a operação assíncrona e retorna antes que a operação for concluída.
    
TBL_BATCH 
  
> Submete-avaliação do filtro até que os dados na tabela são necessários.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O filtro foi aplicado com êxito.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a operação de restrição seja iniciado. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
MAPI_E_TOO_COMPLEX 
  
> A tabela não é possível executar a operação porque o filtro determinado apontado pelo parâmetro _lpRestriction_ é muito complicado. 
    
## <a name="remarks"></a>Comentários

O método **IMAPITable:: Restrict** estabelece uma restrição, ou filtro em uma tabela. Se houver uma restrição anterior, ela é descartada e uma nova aplicada. Aplicar uma restrição não terá nenhum efeito nos dados subjacentes de uma tabela; ele simplesmente altera o modo de exibição, limitando as linhas que podem ser recuperadas às linhas que contêm dados que satisfazem a restrição. 
  
Há vários tipos diferentes de restrições, cada descrita com uma estrutura diferente. A estrutura de [SRestriction](srestriction.md) contém dois membros: um valor que indica o tipo de restrição e a estrutura específica aplicável desse tipo. 
  
Notificações de linhas da tabela que estão ocultas do modo por chamadas para **Restrict** nunca são geradas. 
  
Uma restrição de propriedade em uma propriedade de valores múltiplos funciona como uma restrição em uma propriedade de valor único. Uma propriedade de vários valores a serem usados em uma restrição de propriedade deve ter o sinalizador MVI_FLAG definido. Se ele não tiver esse sinalizador definido, ela é tratada como uma tupla totalmente ordenada. Uma comparação de duas colunas multivaloradas compara os elementos de coluna em ordem, a relação entre as colunas na primeira inequação de emissão de relatórios. Igualdade será retornada somente se as colunas comparadas contêm os mesmos valores na mesma ordem. Se uma coluna tiver valores menos que o outro, a relação relatada é de um valor nulo para o outro valor.
  
Para obter mais informações sobre as restrições, consulte [Sobre restrições](about-restrictions.md).
  
> [!NOTE]
> Se você criar consultas dinâmicas para pesquisar dados no servidor, use o método **FindRow** em vez de usar o método **Restrict** e o método **QueryRows** juntos. O método **Restrict** cria um modo de exibição de cache que é usado para avaliar todas as mensagens adicionados a ou modificado na pasta base. Se um aplicativo cliente usa o método **Restrict** para cada consulta dinâmica, um modo de exibição em cache será criado para cada consulta. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para descartar a restrição atual sem criar um novo, passe NULL no _lpRestriction_.
  
Se outra chamada assíncrona tabela estiver em andamento, causando **Restrict** retornar MAPI_E_BUSY, é possível chamar [IMAPITable::Abort](imapitable-abort.md) para interromper a chamada. 
  
 **Restrict** opera de maneira síncrona, a menos que você defina um dos sinalizadores. Se você definir o sinalizador TBL_BATCH, **Restrict** adia a avaliação da restrição, a menos que você solicitar os dados. Se o sinalizador TBL_ASYNC estiver definido, **Restrict**opera de forma assíncrona, retornando potencialmente antes da conclusão da operação.
  
Todos os indicadores para uma tabela são descartados quando é feita uma chamada para **Restrict** e BOOKMARK_CURRENT, a posição atual do cursor, é definida para o início da tabela. 
  
Se você tentar impor uma restrição de propriedade em uma propriedade que não esteja no conjunto de colunas da tabela, os resultados são indefinidos. Sempre que você não tiver certeza de como para se uma propriedade é suportada em uma tabela, combinar a restrição de propriedade com uma restrição de existir. A restrição verifica a existência da propriedade antes de tentar impor a restrição de propriedade de existir. 
  
Não espera receber uma notificação de tabela em uma linha que tiver sido filtrada de uma tabela devido a uma restrição.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI usa o método **IMAPITable:: Restrict** para definir uma restrição em uma tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::ExpandRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

