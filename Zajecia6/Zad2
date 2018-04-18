#include <iostream>

using namespace std;

namespace pt
{
class Point{
private:
    int x,y;

public:

    int GetX()
    {
        return x;
    }

    int GetY()
    {
        return y;
    }

    Point()
    {
        x = 0;
        y = 0;
    }

    Point(int x, int y)
    {
        this->x = x;
        this->y = y;
    }
};

class Point3D:public Point{
private:
    int z;

public:

    int GetZ()
    {
        return z;
    }

    Point3D(int x, int y, int z) : Point(x , y)
    {
        this->z = z;
    }
};

}

int main(int argc, char *argv[])
{

    return 0;
}
