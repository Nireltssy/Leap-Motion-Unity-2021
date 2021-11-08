# Leap-Motion-Unity-2021

## Erro do Leap Motion ao compilar em ambiente Unity.

- O erro acontece não permitindo dar o Play no ambiente criado com um leap motion, após a importação do CORE.

- Isso acontece pois há uma falha no arquivo Hotkeys.cs fazendo que alguns parâmetos já estejam obsoletos para as novas versões e impedindo que rode o core.

### Erro

O erro aparece na linha de código, como podemos ver na imagem abaixo em vermelho:

![Hotkeys](https://user-images.githubusercontent.com/33674966/140668139-a9c97be9-02a1-4db9-af5a-75545a6857a1.jpg)

## Corrigindo o Erro

### Passos Para Corrigir o Erro
- [ ] Localizar trecho do código que contém erro.
- [ ] Substituir na primeira parte
- [ ] Localizar demais trechos com erro
- [ ] Substituir trechos
- [ ] Apagar comentários do cabeçalho do código

1. Devemos alterar esse trecho para:

```
      GameObject[] objs = Selection.GetFiltered<GameObject>(SelectionMode.Editable);
      if (objs.Length == 0) {
        return;
      }
```
- [X] Localizar trecho do código que contém erro.
- [X] Substituir na primeira parte
- [ ] Localizar demais trechos com erro
- [ ] Substituir trechos
- [ ] Apagar comentários do cabeçalho do código

2. Após alterar esse trecho de código, deve-se alterar todos os demais que aparecerem **_(SelectionMode.ExcludePrefab|SelectionMode.OnlyUserModifiable|SelectionMode.Editable)_** para apenas **_(SelectionMode.Editable)_**

- [X] Localizar trecho do código que contém erro.
- [X] Substituir na primeira parte
- [X] Localizar demais trechos com erro
- [X] Substituir trechos
- [ ] Apagar comentários do cabeçalho do código

3. Apagar os comentários presente nas linhas **1** a **8**

- [X] Localizar trecho do código que contém erro.
- [X] Substituir na primeira parte
- [X] Localizar demais trechos com erro
- [X] Substituir trechos
- [X] Apagar comentários do cabeçalho do código

## Conclusão

- Pronto após esses passos o leap motion será executado normalmente, podendo assim carregar os outros packages.

     ![4185b53d71c0d7e7995f51aee3c6cbcd](https://user-images.githubusercontent.com/33674966/140669197-488eba36-8c8b-4c48-8f9c-a092e91509b5.gif)

