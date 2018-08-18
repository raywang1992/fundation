"""
快速排序
最优时间复杂度：O(nlogn)
最坏时间复杂度：O(n2)
稳定性：不稳定

"""
import time
import random

def quick_sort(list, star, end):
    # 递归的退出条件
    if star >= end:
        return

    # low为序列左边的由左向右移动的游标
    low = star

    # high 为序列右边的由右向左移动的游标
    high = end

    # 设定其实元素为要寻找位置的基准元素
    mid_value = list[star]

    while low < high:
        # 如果low 与high 未重合，high 指向的元素不比基准元素小，则high向左移
        while low < high and list[high] >= mid_value:
            high -= 1

        # 将high 指向的元素放到low 的位置上
        list[low] = list[high]

        # 如果low与high未重合，low指向的元素比基准元素小，low的向右移
        while high > low and list[low] < mid_value:
            low += 1

        # 将low指向的元素放到high的位置上
        list[high] = list[low]

    # 退出循环后，low 与high重合，此时所指位置为基准元素的正确位置
    # 循环退出时 将基准元素放到该位置
    list[low] = mid_value

    # 对基准元素的左边的子序列进行快速排序
    quick_sort(list, star, low-1)

    # 对基准元素右边的子序列进行快速排序
    quick_sort(list, low+1, end)


def new_num(lis):
    """随机生成50个数加入列表中"""
    for i in range(50):
        j = random.randint(0,10000)
        lis.append(j)


if __name__ == '__main__':

    first_time = time.time()
    # 空列表
    lis = []

    # 随机函数添加到列表中
    new_num(lis)

    # 列表排序
    quick_sort(lis, 0, len(lis)-1)

    print(lis)

    # 结束时间
    last_time = time.time()

    print("共用时%s" % (last_time - first_time))
    
