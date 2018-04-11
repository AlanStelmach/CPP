#include <iostream>

using namespace std;

class Polygon
{
public:
    struct Point {
        double x;
        double y;
    };

    Polygon()
    {
        size = 4;
        count = 0;
        points = new Point*[4];
    };

    Polygon(int size)
    {
        if(size%4 != 0)
            size = size + (4-size%4);
        this->size = size;
        count = 0;
        points = new Point*[size];
    };

    Polygon(const Polygon $polygon)
    {
        this->count = polygon.count;
        this->size = polygon.size;
        points = new Point*[size];
        for(int i = 0; i<count; i++)
        {
            points[i] = new Point();
            points[i]->x = polygon.points[i]->x;
            points[i]->y = polygon.points[i]->y;
        }
    }

    ~Polygon()
    {
        for(int i = 0; i<count; i++)
            delete points[i];
        delete points;
    }

    void add(Point point)
    {
        if(count == size)
        {
            Point ** tmp = points;
            size +=4;
            points = new Point*[size];
            for(int i = 0; i < count; i++)
                points[i] = tmp[i];
            delete tmp;
        }
    }

    Point* getPoint(int index)
    {
        if(index<count)
            return points[index];
        else
            return NULL;
    }

private:
    Point **points;
    int count, size;

};

int main(int argc, char *argv[])
{
    Polygon *polygon = new Polygon(25);
    Polygon::Point p;
    p.x = 8;
    p.y = 9;
    polygon.add(p);
    Polygon::Point *p2 = polygon->getPoint(0);
    cout << p2->x << " " << p2->y << endl;

    return 0;
}
