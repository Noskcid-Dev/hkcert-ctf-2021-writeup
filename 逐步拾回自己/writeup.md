# 逐步拾回自己

| Info | Value |
| :--- | :-----: |
| Categories | #★☆☆☆☆ #REVERSE #MISC |
| Score | 50 |
| Total Solve (Rate) | 234/240 (28.3%) |

## Description

Retrieve the flag step by step.

### Attachments
excel_4891c2b27e2312569280036715a101b9.zip

## School Solves
| Overall Order | School Order | Name | Solved at |
| :-: | :-: | :-: | :-: |
| 67 | 1 |  S0092 - Immaculate Heart of Mary College | 2021-11-12 18:00:05:322 |
| - | - |  S0090 - Immaculate Heart of Mary College | Unsolved |
| - | - | S0091 - Immaculate Heart of Mary College | Unsolved |
| - | - | S0096 - Immaculate Heart of Mary College | Unsolved |

Total: 1/4 (25%)

## Writeup
First we entered `hkcert21{}` as we know that are the flag format, then we brute forced our way through by running the following VB script:

```vb
Function try(n)
    If n Cells(1, 2) Then
        found = True
        For i = 4 To 29
            if Cells(22, i) <> Cells (23, i) Then
                found = False
            End if
        Next
        For i = 14 To 21
            If Cells(i, 30) <> Cells(i, 31) Then
                found = False
            End If
        Next
        If found = True Then
        MsgBoxCells(1, 2)
        End If

        try = 0
    Else
        For ascii = 33 To 126
            If ascii <> 39 Then
            Cells(2, n).Value = Chr(ascii)
            If Cells(22, n - 1) = Cells(23, n - 1) Then
                try (n + 1)

            End If
            End If
        Next
    End If
End Function
```
and we got the flag.

## Flag
`hkcert21{funny_excel_rev}`