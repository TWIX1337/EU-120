import numpy as np


def task1(a, n, m):
    b = np.fabs(a)
    index = np.argmax(b.max(axis=0))
    print((a[:, index]).max())


def task2(a, n, m):
    print(a.mean(axis=1))
    print(max(a.mean(axis=1)))


def task3(a, n, m):
    b = np.fabs(a)
    index = np.argmax(b.max(axis=0))
    print((a[:, index]).min())


def task4(a, n, m):
    print(min(a.mean(axis=1)))


def task5(a, n, m):
    col = a.mean(axis=0)
    print(col)
    col = (col[np.newaxis, :])
    print(np.vstack([a, col]))
    a = (np.vstack([a, col]))
    row = a.mean(axis=1)
    row = (row[np.newaxis, :])
    row = row.reshape(n + 1, 1)
    a = (np.hstack([a, row]))
    print(a)


def task6(a, n, m):
    sum_elem = a.sum()
    list_sum_col = []
    for i in range(m):
        sum_col = sum(a[:, i])
        list_sum_col.append(sum_col)
        print(sum_col * 100 / sum_elem)
    npa = np.asarray(list_sum_col)
    npa = (npa[np.newaxis, :])
    a = (np.vstack([a, npa]))
    print(a)


def task7(a, n, m):
    sum_elem = a.sum()
    list_sum_row = []
    for i in range(n):
        sum_row = sum(a[i, :])
        list_sum_row.append(sum_row * 100 / sum_elem)
        print(sum_row * 100 / sum_elem)
    row = np.asarray(list_sum_row)
    row = (row[:, np.newaxis])
    a = np.append(a, row, axis=1)
    print(a)


def task8(a, n, m):
    col = []
    row = []
    for i in range(m):
        b = a[:, i]
        col.append(sum(i < 0 for i in b))
    col = np.asarray(col)
    col = (col[np.newaxis, :])
    a = np.append(a, col, axis=0)

    for i in range(n + 1):
        b = a[i, :]
        row.append(sum(i < 0 for i in b))
    row = np.asarray(row)
    row = (row[:, np.newaxis])
    a = np.append(a, row, axis=1)
    print(a)


def task9(a, n, m, l, k):
    count_top = 0
    count_left = 0
    b = a[:l, :].copy()
    for index, value in np.ndenumerate(b):
        if value == 0:
            count_top += 1
    print("The first " + str(l) + " lines: " + str(count_top) + " zeros")

    c = a[:, :k].copy()
    for index, value in np.ndenumerate(c):
        if value == 0:
            count_left += 1
    print("The first " + str(k) + " columns: " + str(count_top) + " zeros")


def task10(a, n, m, k):
    col = a[:, k]
    for i in range(m):
        if i == k:
            continue
        a[:, i] = col * a[:, i]
    print(a)


def task11(a, n, m, l):
    row = a[l, :]
    for i in range(n):
        if i == l:
            continue
        a[i, :] = row + a[i, :]
    print(a)


def task12(a, n, m):
    a.astype()
    max_elem = a.max(axis=1)
    print(max_elem)
    for i in range(n):
        for j in range(m):
            a[i][j] /= max_elem[i]
    print(a)


def task13(a, n, m):
    for i in range(m):
        max_elem = max(a[:, i])
        #print(max_elem)
        a[:, i] /= max_elem
    print(a)


def task14(a, n, m):
    print(a.max())
    a = a / (a.max())
    print(a)


def task15(a, n, m, h):
    contains = []
    not_contains = []
    for i in range(m):
        print(a[:, i])
        if h in a[:, i]:
            contains.append(i)
        else:
            not_contains.append(i)
    print('Contains: {}, Not contains: {}, value: {}'.format(contains, not_contains, h))


def task16(a, n, m, l):
    a = np.delete(a, l, axis=0)
    print(a)


def task17(a, n, m, l):
    a = np.insert(a, [l], [1], axis=0)
    print(a)


def task18(a, n, m):
    # n must less then m
    sumMain = 0
    sumSecondary = 0
    for i in range(N):
        sumMain += a[i][i]
        sumSecondary += a[i][n - i - 1]
    print(sumMain)
    print(sumSecondary)


def task19(a, n):
    sum_elem_down = 0
    sum_elem_up = 0
    for i in range(1, n):
        sum_elem_down += a[i][i - 1]
        sum_elem_up += a[i - 1][i]
    print(sum_elem_down + sum_elem_up)


def task20(a, n):
    sum_elem_down = 1
    sum_elem_up = 1
    for i in range(0, n-1):
        sum_elem_down *= a[n-i-1][i+1]
        sum_elem_up *= a[i][n-i-2]
    print(sum_elem_down * sum_elem_up)


def task21(a, n):
    for i in range(1, n):
        _sum = a[i][i - 1] + a[i - 1][i]
        a.itemset((i, i-1), _sum // 2)
        a.itemset((i-1, i), _sum // 2)
    print(a)


def task22(a, n, m):
    b = a.sum(axis=1)
    b %= 2
    b = (b[np.newaxis, :])
    b = b.reshape(n, 1)
    print(np.hstack([a, b]))


def task23(a, n):
    sum_elem = 0
    mul_elem = 1
    for i in range(0, n):
        sum_elem += a[i, i + 1:].sum()

    for i in range(0, n - 1):
        for j in range(0, n - i - 1):
            mul_elem *= a[i][j]
    print("Sum_elem= " + str(sum_elem) + " Mul_elem= " + str(mul_elem))


def task24(a, n, m, l, k):
    print(a[:l, :k].sum())
    print(a[:l, k:].sum())
    print(a[l:, :k].sum())
    print(a[l:, k:].sum())


def task25(a, n, m):
    col = []
    row = []

    for i in range(m):
        col.append(np.count_nonzero(a[:, i] == 0))
    col = np.asarray(col)
    col = (col[np.newaxis, :])
    a = np.append(a, col, axis=0)

    for i in range(n + 1):
        row.append(np.count_nonzero(a[i, :] == 0))
    row = np.asarray(row)
    row = (row[:, np.newaxis])
    a = np.append(a, row, axis=1)
    print(a)


def task26(a, n, m, l, k):
    print(a[:l, :k].mean())
    print(a[:l, k:].mean())
    print(a[l:, :k].mean())
    print(a[l:, k:].mean())


def task27(a, n, m, h):
    contains = []
    not_contains = []
    for i in range(n):
        if h in a[i, :]:
            contains.append(i)
        else:
            not_contains.append(i)
    print('Contains: {}, Not contains: {}, value: {}'.format(contains, not_contains, h))


def task28(a, n, m, k):
    a = np.delete(a, (k), axis=1)
    print(a)


def task29(a, n, m, k):
    b = np.random.randint(-15, 15, size=(n, 1))
    c = np.insert(a, k, values=b[:, 0], axis=1)
    print(c)


def task30(a, n, m):
    col = []
    for i in range(m):
        b = a[:, i]
        sum_abs = 0
        sum = 0
        for j in range(n):
            if b[j] < 0:
                sum_abs += abs(b[j])
            else:
                sum += b[j]
        col.append(sum_abs - sum)
    col = np.asarray(col)
    col = (col[np.newaxis, :])
    a = np.append(a, col, axis=0)
    print(a)


def task31(a, n, m):
    row = []
    for i in range(n):
        b = a[i, :]
        sum_abs = 0
        sum = 0
        for j in range(m):
            if b[j] < 0:
                sum_abs += abs(b[j])
            else:
                sum += b[j]
        row.append(sum_abs - sum)
    row = np.asarray(row)
    row = (row[:, np.newaxis])
    a = np.append(a, row, axis=1)
    print(a)


if __name__ == '__main__':
    N = 5
    M = 6

    A = np.random.randint(1, 25, size=(N, M))

    # Some function must called:
    # A = np.random.randint(-15, 15, size=(N, M))
    # B = np.random.random(size=(N, M))
    # B *= 100
    # B = np.around(B, decimals=2)
    # For example:
    # task13(B, N, M)
    task6(A, N, M)
